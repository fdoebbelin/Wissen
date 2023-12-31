![](http://obj-cache.cloud.ruanbekker.com/minio-black.png)

In our previous post, we have [Setup Minio Server](https://sysadmins.co.za/run-your-self-hosted-s3-service-with-minio-on-docker-swarm/) which is a self-hosted alternative to Amazon's S3 Service.

We will go through some basic examples on working with the Python SDK, to interact with Minio.

**Installing the Minio Python Library:**

Ensure that Python and Pip is installed, the install the Python Minio Library:

```
$ python3 -m venv venv
$ source venv/bin/activate
(venv)$ pip install minio

```

**Create a Bucket:**

Enter the Python Interpreter and Create a S3 Bucket on your Minio Server:

```
>>> from minio import Minio
>>> client = Minio('10.0.0.2:9000', access_key='ASDASDASD', secret_key='ASDASDASD', secure=False)
>>> client.make_bucket('pythonbucket', location='us-west-1')

```

**List Buckets:**

I have also created a bucket from my previous post, so we should have 2 buckets:

```
>>> buckets = client.list_buckets()
>>> for bucket in buckets:
...     print(bucket).name
...
news3bucket
pythonbucket

```

**Put Objects to your Bucket:**

Write a string to a file, then upload the file to 2 different destination objects. The arguments is: BucketName, Destination, Source.

```
>>> data = open('file.txt', 'w')
>>> data.write('This is some text' + '\n')
>>> data.close()

>>> client.fput_object('pythonbucket', 'bucket/contents/file.txt', 'file.txt')
'6b8c327f0fc6f470c030a5b6c71154c5'
>>> client.fput_object('pythonbucket', 'bucket/contents/file2.txt', 'file.txt')
'6b8c327f0fc6f470c030a5b6c71154c5'

```

**List Objects in your Bucket:**

List the objects in your bucket:

```
>>> objects = client.list_objects('pythonbucket', prefix='bucket/contents/', recursive=True)
>>> for obj in objects:
>>> for obj in objects:
...     print(obj.object_name, obj.size)
...
('bucket/contents/file.txt', 18)
('bucket/contents/file2.txt', 18)

```

**Remove Objects from your Bucket:**

Remove the objects from your Bucket, the list your bucket to verify that they are removed:

```
>>> client.remove_object('pythonbucket', 'bucket/contents/file.txt')
>>> client.remove_object('pythonbucket', 'bucket/contents/file2.txt')

>>> for obj in objects:
...     print(obj.object_name, obj.size)
...
>>>

```

**Remove the Bucket:**

Remove the Bucket that we created:

```
>>> client.remove_bucket('pythonbucket')
>>> exit()

```

**Resources:**

Minio has some great documentation, for more information on their SDK:

- [https://docs.minio.io/docs/python-client-api-reference](https://docs.minio.io/docs/python-client-api-reference)