As described in the Docker documentation on [Working with Volumes](http://docs.docker.io/en/latest/use/working_with_volumes/) there is the concept of so-called _data-only_ containers, which provide a volume that can be mounted into multiple other containers, no matter whether the data-only container is actually running or not.

Basically, this sounds awesome. But there is one thing I do not understand.

These volumes (which do _not_ explicitly map to a folder on the host for portability reasons, as the documentation states) are created and managed by Docker in some internal folder on the host (`/var/docker/volumes/…`).

Supposed I use such a volume, and then I need to migrate it from one host to another - how do I port the volume? AFAICS it has a unique ID - can I just go and copy the volume and its according data-only container to a new host? How do I find out which files to copy? Or is there some support built-in to Docker that I did not discover yet?

asked Feb 6 '14 at 8:20

[![](_resources/7ae9b432531de46073888f1a49c2391c.jpg)](https://stackoverflow.com/users/1333873/golo-roden)

[Golo Roden](https://stackoverflow.com/users/1333873/golo-roden)Golo Roden

90.8k6666 gold badges221221 silver badges336336 bronze badges

The official answer is now available here:

[Sharing Directories using Volumes](https://docs.docker.com/v17.03/engine/tutorials/dockervolumes/#backup-restore-or-migrate-data-volumes)

In the "Backup, restore, or migrate data volumes" section you have:

**BACKUP:**

```
sudo docker run --rm --volumes-from DATA -v $(pwd):/backup busybox tar cvf /backup/backup.tar /data

```

*   `--rm`: remove the container when it exits
*   `--volumes-from DATA`: attach to the volumes shared by the DATA container
*   `-v $(pwd):/backup`: bind mount the current directory into the container; to write the tar file to
*   `busybox`: a small simpler image - good for quick maintenance
*   `tar cvf /backup/backup.tar /data`: creates an uncompressed tar file of all the files in the /data directory

**RESTORE:**

```
# create a new data container
$ sudo docker create -v /data --name DATA2 busybox true
# untar the backup files into the new container᾿s data volume
$ sudo docker run --rm --volumes-from DATA2 -v $(pwd):/backup busybox tar xvf /backup/backup.tar
data/
data/sven.txt
# compare to the original container
$ sudo docker run --rm --volumes-from DATA -v `pwd`:/backup busybox ls /data
sven.txt

```

[![](_resources/photo.jpg)](https://stackoverflow.com/users/9089002/anthony-ward)

answered May 21 '14 at 9:01

[![](_resources/8htsx.png)](https://stackoverflow.com/users/204626/tommasop)

You can export the volume to tar and transfer to another machine. And import the data with tar on the second machine. This does not rely on implementation details of the volumes.

```
# you can list shared directories of the data container
docker inspect <data container> | grep "/vfs/dir/"

# you can export data container directory to tgz
docker run --cidfile=id.tmp --volumes-from <data container> ubuntu tar -cO <volume path> | gzip -c > volume.tgz

# clean up: remove exited container used for export and temporary file
docker rm `cat id.tmp` && rm -f id.tmp

```

answered Feb 6 '14 at 21:32

[![](_resources/b14f45eef5521771da8d792a4009b906.png)](https://stackoverflow.com/users/39726/jiri)

[Jiri](https://stackoverflow.com/users/39726/jiri)Jiri

14.9k44 gold badges4747 silver badges6363 bronze badges

Extending the official answer from [Docker docs](https://docs.docker.com/engine/userguide/dockervolumes/#backup-restore-or-migrate-data-volumes) and the [top answer here](https://stackoverflow.com/a/23778599/1046584), you can have following aliases in your .bashrc or .zshrc

```
# backup files from a docker volume into /tmp/backup.tar.gz
function docker-volume-backup-compressed() {
  docker run --rm -v /tmp:/backup --volumes-from "$1" debian:jessie tar -czvf /backup/backup.tar.gz "${@:2}"
}
# restore files from /tmp/backup.tar.gz into a docker volume
function docker-volume-restore-compressed() {
  docker run --rm -v /tmp:/backup --volumes-from "$1" debian:jessie tar -xzvf /backup/backup.tar.gz "${@:2}"
  echo "Double checking files..."
  docker run --rm -v /tmp:/backup --volumes-from "$1" debian:jessie ls -lh "${@:2}"
}
# backup files from a docker volume into /tmp/backup.tar
function docker-volume-backup() {
  docker run --rm -v /tmp:/backup --volumes-from "$1" busybox tar -cvf /backup/backup.tar "${@:2}"
}
# restore files from /tmp/backup.tar into a docker volume
function docker-volume-restore() {
  docker run --rm -v /tmp:/backup --volumes-from "$1" busybox tar -xvf /backup/backup.tar "${@:2}"
  echo "Double checking files..."
  docker run --rm -v /tmp:/backup --volumes-from "$1" busybox ls -lh "${@:2}"
}

```

Note that the backup is saved into `/tmp`, so you can move the backup file saved there between docker hosts.

There is also two pairs of backup/restore aliases. One using compression and debian:jessie and other with no compression but with busybox. Favor using compression if the files to backup are big.

answered Jan 13 '16 at 21:06

[![](_resources/a12f24dc02bccd33ed96beeede302b38.png)](https://stackoverflow.com/users/1046584/lu%c3%ads-bianchin)

[Luís Bianchin](https://stackoverflow.com/users/1046584/lu%c3%ads-bianchin)Luís Bianchin

1,56011 gold badge1717 silver badges3232 bronze badges

I'll add another recent tool here from IBM which is actually made for the volume migration from one container host to another. This is a currently on-going project. So, you may find a different version with additional features in future.

**Cargo** was developed to migrate containers from one host to another host along with their data with minimal downtime. Cargo uses data federation capabilities of **union filesystem** to create a unified view of data (mainly the root file system) across the source and target hosts. This allows Cargo to start up a container almost immediately (within milliseconds) on the target host as the data from source root file system gets copied to target hosts either on-demand (using a **copy-on-write (COW)** partition) or lazily in the background **(using rsync)**.

Important points are: - a **`centralized`** server handles the migration process

The link to the project is given here:

```
https://github.com/nadgowdas/cargo

```

answered Dec 1 '17 at 14:36

[![](_resources/SVNx7.jpg)](https://stackoverflow.com/users/3959912/arif-a)

[Arif A.](https://stackoverflow.com/users/3959912/arif-a)Arif A.

55633 silver badges1111 bronze badges

In case your machines are in different VPCs or you want to copy from/to local machine (like in my case) you can use [dvsync](https://github.com/suda/dvsync) I created. It's basically [ngrok](https://ngrok.com/) combined with `rsync` over SSH packaged into two small (both ~25MB) images. First, you start the `dvsync-server` on a machine you want to copy data from (You'll need the `NGROK_AUTHTOKEN` which can be obtained from [ngrok dashboard](https://dashboard.ngrok.com/auth)):

```
$ docker run --rm -e NGROK_AUTHTOKEN="$NGROK_AUTHTOKEN" \
  --mount source=MY_VOLUME,target=/data,readonly \
  quay.io/suda/dvsync-server

```

Then you can start the `dvsync-client` on the machine you want to copy the files to, passing the `DVSYNC_TOKEN` shown by the server:

```
docker run -e DVSYNC_TOKEN="$DVSYNC_TOKEN" \
  --mount source=MY_TARGET_VOLUME,target=/data \
  quay.io/suda/dvsync-client 

```

Once the copying will be done, the client will exit. This works with Docker CLI, Compose, Swarm and Kubernetes as well.

answered Jul 11 '18 at 21:32

[![](_resources/cba56198463ece8d5c1cc1d6a353ddbd.jpg)](https://stackoverflow.com/users/83055/suda)

[suda](https://stackoverflow.com/users/83055/suda)suda

2,31011 gold badge2222 silver badges3636 bronze badges

## Not the answer you're looking for? Browse other questions tagged [docker](https://stackoverflow.com/questions/tagged/docker "show questions tagged 'docker'") or [ask your own question](https://stackoverflow.com/questions/ask).