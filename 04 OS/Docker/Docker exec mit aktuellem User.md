Docker führt Kommandos im Container immer als root als, wenn keine User-ID übergeben wird

```
$ docker container exec -it --user "$(id -u):$(id -g)" web1 touch hi.txt
```