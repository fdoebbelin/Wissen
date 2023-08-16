Since HTTP driven applications are stateless, sessions provide a way to store information about the user across requests, for example when you get login in a laravel website your session data is caching in files by default and when you have 3 laravel backend for example 3 replica in kubernetes when you request another webpage you may login or not because your session is not shared among pods.

For solving session problem we have two ways :

- using sticky session in loadbalancer
- sharing sessions among pods

F<a id="rmm"></a><a id="rmm"></a><a id="rmm"></a><a id="rmm"></a><a id="rmm"></a><a id="rmm"></a><a id="rmm"></a><a id="rmm"></a>ortunately, nginx ingress [support](https://kubernetes.github.io/ingress-nginx/examples/affinity/cookie/) sticky sessions you can simply add this annotation in your ingress‍‍‍‍‍

 <a id="d296"></a>nginx.ingress.kubernetes.io/affinity: "cookie"  
    nginx.ingress.kubernetes.io/session-cookie-name: "route"  
    nginx.ingress.kubernetes.io/session-cookie-expires: "172800"  
    nginx.ingress.kubernetes.io/session-cookie-max-age: "172800"

One of the problems of this method is the opposite of using round-robin user always use the first pod she or he connected.

Sharing sessions among pods another way that I prefer. you can change default [session driver](https://laravel.com/docs/5.1/session) and using Redis driver for caching sessions.

Laravel logs and coordinating them is important when you have multi-instance in [this post](https://medium.com/@b3hroozam/laravel-5-6-and-docker-logs-3741349abf75) I completely explained how it can happen in kubernetes.

but in summary you have multiple options:

- using [sentry](https://docs.sentry.io/clients/php/integrations/) as a bug reporter
- coordinate logs with EFK or ELK stack
- using laravel logs drivers and send directly log messages to [fluentd](https://github.com/ytake/Laravel-FluentLogger) or [elasticsearch](https://matthewdaly.co.uk/blog/2018/06/03/logging-to-the-elk-stack-with-laravel/)

Most of laravel developers prefer using the default storage path `storage/app/public` so persisting this data is important.

Kubernetes for [persisting data](https://kubernetes.io/docs/concepts/storage/persistent-volumes/) have many options you can choose.

Small business uses php or MariaDB in default but scaling php application tragically depends on your resources and configurations. **this articles and tools about performance tuning MariaDB and php help you**.

Before deploying the application to k8s you need to ensure that application is worked so for you the better option is using docker-compose for Development and Kubernetes for Production.

**In this GitHub repository, I will put all docker-compose and BaseImage and Kubernetes templates that need for deploying laravel to k8s.**

First of all, we have to create a proper multi-stage Dockerfile and BaseImage.

Docker introduces multi-stage build in 17.05 version, using laravel cache layers and change the only app layer help reduce the image size, for me 1GB to 200MB 😲.

**This is a BaseImage and a script for fixing project permissions.**

**Dockerfile for production depending on using nodejs modules or not.**

I will assume you are familiar with kubernetes and architecture.

**This is what we want to do**

![](_resources/1_YV0pYCBu4QYDEt-0c_N9VQ_6ff0c86cb66e44588a2f99591.png)

Deploying Laravel application to K8S workflow

By default, Laravel using MySQL as Database but I will prefer using MariaDB.

Before deploying MariaDB we need to create password Secret, I prefer imperative or command line mode for creating Secrets but in complicated scenarios, we have to use Declarative YAML files.

**The first step is to create namespace:**

<a id="35dd"></a>kubectl create namespace laravel

**The second step is to create a secret password**

<a id="8b99"></a>kubectl -n laravel create secret generic laravel-mariadb-pass --from-literal=password=laravel

**The third step is to labeling node as in this tutorial I am using host path persistent storage**

<a id="01dd"></a>kubectl get nodes  
kubectl label nodes &lt;your-node-name&gt; database=true

**And finally, apply** `Kubernetes/DataBase/MariaDB.yaml` **file**

<a id="ee6e"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/DataBase/MariaDB.yaml

after create, tag and push your image to registry its time to deploy the project

As you saw in the image above we most create configmaps and persistent storage.

so applying

<a id="e2f3"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/configmaps.yaml<a id="ee73"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/Storage.yaml

**Note that I am using NFS as the persistent volume you can change it depending on your need.**

applying services and deployment and ingress are in the last step complete your journey to create a kubernetes laravel project

<a id="8d5d"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/Application-Deployment.yaml<a id="3c3d"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/Service.yaml<a id="ec38"></a>kubectl apply -f Laravel-kubernetes-example/Kubernetes/ingress.yaml