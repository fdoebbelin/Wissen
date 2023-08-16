Running Laravel on Kubernetes should be relatively straightforward for someone comfortable with both components (especially if you've been running Laravel in containers for some time).

For better or for worse, I made the leap from Laravel on VMs to Laravel in Containers and on Kubernetes at the same time, so there were some extra hoops to jump through.

* * *

**Dockerizing Laravel**

The first thing to do was to set up the base docker container for Laravel with all of the dependencies it would need to run. Below is the `.dockerignore` and `Dockerfile` I built that provides all of the required packages (plus ImageMagick) that Laravel needs to run successfully.

```
.git
.idea
.env
node_modules
storage/framework/cache/**
storage/framework/sessions/**
storage/framework/views/**

```

```
FROM php:7.3-fpm

WORKDIR /var/www

RUN apt-get update && apt-get install -y libmcrypt-dev zip unzip git \
    libmagickwand-dev --no-install-recommends \
    && pecl install imagick \
    && docker-php-ext-enable imagick \
    && docker-php-ext-install pdo_mysql pcntl bcmath

COPY . /var/www

RUN chown -R www-data:www-data \
        /var/www/storage \
        /var/www/bootstrap/cache

RUN mkdir -p /tmp/storage/bootstrap/cache \
    && chmod 777 -R /tmp/storage/bootstrap/cache

```

The base container I am using is the [PHP-FPM](https://php-fpm.org/) image, which isn't a web server, but rather is the process manager generally seen as the defacto for modern deployments – this container will be coupled with an [Nginx](https://www.nginx.com/) container which will be actual web serving component of this.

* * *

**Dockerizing Nginx**

The Nginx container is just the alpine container and a custom server configuration block.

The only "interesting" configuration here is the change from the default buffer configuration (`fastcgi_buffers` and `fastcgi_buffer_size`) to account for Laravel's large header payloads.

*For instructions on how to run TLS to the NGINX container, check out my [End-to-End Encryption with Nginx and Kubernetes](https://lorenzo.aiello.family/end-to-end-encryption-with-nginx-and-kubernetes) blog post.*

```
FROM nginx:alpine

ADD vhost.conf /etc/nginx/conf.d/default.conf
```

```
server {
    listen 80;
    index index.php index.html;
    root /var/www/public;

    location / {
        try_files $uri /index.php?$args;
    }

    location ~ \.php$ {
        fastcgi_split_path_info ^(.+\.php)(/.+)$;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_index index.php;
        fastcgi_buffers 16 16k; 
        fastcgi_buffer_size 32k;
        include fastcgi_params;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        fastcgi_param PATH_INFO $fastcgi_path_info;
    }
}
```

* * *

**Deploying on Kubernetes**

Now that it's containerized, built, and hopefully stored someplace, you can deploy it to Kubernetes. The following is an example [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/), [PodAutoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/), and [LoadBalancer](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/) for the service.

You should now have your "Hello World" application up and running.

```
---
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: web
spec:
  replicas: 3
  strategy:
    rollingUpdate:
      maxSurge: 1
      maxUnavailable: 1
  minReadySeconds: 5
  template:
    metadata:
      labels:
        app: web
    spec:
      containers:
        - name: laravel
          image: ##CONTAINER_IMAGE##
          ports:
            - containerPort: 9000
          resources:
            requests:
              cpu: 250m
            limits:
              cpu: 500m
        - name: nginx
          image: nginx:alpine
          ports:
            - containerPort: 80
---
apiVersion: autoscaling/v1
kind: HorizontalPodAutoscaler
metadata:
  name: web
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: web
  minReplicas: 3
  maxReplicas: 20
  targetCPUUtilizationPercentage: 50
---
apiVersion: v1
kind: Service
metadata:
  name: loadbalancer
spec:
  type: LoadBalancer
  ports:
    - port: 80
  selector:
    app: web
```

* * *

**Database Migrations**

To get database migrations running, you can use the following Kubernetes [Job](https://kubernetes.io/docs/tasks/job/).

*Note: Unfortunately, this implementation isn't particularly ideal because it requires you to first delete the job as part of your CI/CD process before it can be redeployed. Please let me know if you have a better way to do it.*

```
---
apiVersion: batch/v1
kind: Job
metadata:
  name: artisan-migration
spec:
  ttlSecondsAfterFinished: 300
  backoffLimit: 3
  template:
    spec:
      restartPolicy: Never
      containers:
        - name: laravel
          image: ##CONTAINER_IMAGE##
          envFrom:
            - configMapRef:
                name: laravel-envvars
          command: ["/usr/local/bin/php", "artisan", "migrate", "--force"]
```

* * *

**Scheduled Tasks**

Most applications will require some scheduled tasks to run, which can be easily set up with a Kubernetes [Cronjob](https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/).

```
---
apiVersion: batch/v1beta1
kind: CronJob
metadata:
  name: cronjob
spec:
  schedule: "*/1 * * * *"
  jobTemplate:
    spec:
      template:
        spec:
          restartPolicy: OnFailure
          containers:
            - name: laravel
              image: ##CONTAINER_IMAGE##
              command: ["/usr/local/bin/php", "artisan", "schedule:run"]
```

* * *

**Laravel Horizon**

When your use case needs event-driven processing, and you want to use [Laravel Horizon](https://laravel.com/docs/6.x/horizon), you can quickly get it up and running with just another Kubernetes Deployment.

```
---
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: horizon-worker
spec:
  replicas: 3
  template:
    metadata:
      labels:
        app: horizon-worker
    spec:
      containers:
        - name: laravel
          image: ##CONTAINER_IMAGE##
          command: ["/usr/local/bin/php", "artisan", "horizon
          lifecycle:
            preStop:
              exec:
                command: ["/usr/local/bin/php", "artisan", "horizon:terminate"]
```

* * *

Last, and certainly not least, I want to touch on Secrets management very briefly. It's a vast topic that warrants it's own blog post, but there are many ways to plug environment variables into the Kubernetes runtime. Still, I will emphasize that you should **NEVER** copy the production `.env` file into your container.

- [Kubernetes ConfigMaps](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
- [Hashicorp Vault Agents](https://learn.hashicorp.com/vault/identity-access-management/vault-agent-k8s)