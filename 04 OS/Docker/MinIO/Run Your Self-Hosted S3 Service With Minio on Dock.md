Minio is a distributed object storage server built for cloud applications, which is similar to Amazon's S3 Service.

Today, we will create the server on docker swarm, as I don't currently have a external data store like GlusterFS / NFS etc, I will host the data on the manager node, and set a constraint for the service so that the service can only run on the manager node.

**Prepare the Data Directory:**

I will only rely on the manager node for my data, so on my manager node:

```bash
$ mkdir -p /mnt/data

```

**Create the Service:**

If you have a Replicated Gluster Volume or NFS which is mounted throughout your docker swarm, you can create the directory path for it, and the update your `--mount` source path to your external data store. In my case, I will just point it to my manager node's `/mnt/data` path as I have setup the service to only run on the one manager node in my swarm:

```bash
$ docker service create \
--name minio \
--network appnet \
--replicas 1 \
--publish 9000:9000 \
--constraint 'node.role==manager' \
-e "MINIO_ACCESS_KEY=ASDFASDFASDF" \
-e "MINIO_SECRET_KEY=ASDFASDFASDF" \
--mount "type=bind,source=/mnt/data,target=/data" \
minio/minio server /data

```

**Install the AWS CLI Tools:**

We will use the awscli tools to interact with our Minio Server:

```bash
$ pip install awscli

```

**Configure the Client:**

Configure the awscli client with the access details that we passed in our docker service:

```bash
$ aws configure --profile minio
AWS Access Key ID []: ASDFASDFASDF
AWS Secret Access Key []: ASDFASDFASDF
Default region name []: us-west-1
Default output format []: json

```

**Create the Bucket:**

Create a New Bucket, in this case `news3bucket`

```bash
$ aws --profile minio --endpoint-url http://MINIO-IP:9000 s3 mb s3://news3bucket
make_bucket: news3bucket

```

**List Buckets:**

List our endpoint, to see the buckets on our server:

```bash
$ aws --profile minio --endpoint-url http://MINIO-IP:9000 s3 ls /
2017-09-08 15:01:40 news3bucket

```

**Upload an Object to your Bucket:**

We will upload an image `awsddb-1.png` to our new bucket:

```bash
$ aws --profile minio --endpoint-url http://MINIO-IP:9000 s3 cp awsddb-1.png s3://news3bucket/
upload: ./awsddb-1.png to s3://news3bucket/awsddb-1.png

```

**List Bucket:**

List your bucket, to see the uploaded object:

```bash
$ aws --profile minio --endpoint-url http://MINIO-IP:9000 s3 ls s3://news3bucket
2017-09-08 15:03:11      19851 awsddb-1.png

```

**Download Object:**

Download the image from your Bucket, and set the local file to `file.png`:

```bash
$ aws --profile minio --endpoint-url http://MINIO-IP:9000 s3 cp s3://news3bucket/awsddb-1.png file.png
download: s3://news3bucket/awsddb-1.png to ./file.png

```

**Web Access:**

You can also access Minio's Web Interface on the port that you have exposed, in my case: `http://MINIO-IP:9000/minio/`

**Resources:**

- [https://www.minio.io/](https://www.minio.io/)
- [https://docs.minio.io/docs/minio-docker-quickstart-guide](https://docs.minio.io/docs/minio-docker-quickstart-guide)
- [https://github.com/minio/minio/blob/master/README.md](https://github.com/minio/minio/blob/master/README.md)
- [https://github.com/arschles/minio-howto/blob/master/aws-cli-with-minio-server.md](https://github.com/arschles/minio-howto/blob/master/aws-cli-with-minio-server.md)