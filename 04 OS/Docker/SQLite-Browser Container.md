```
version:  "3"
  services:
    sqlitebrowser:
	    image:  lscr.io/linuxserver/sqlitebrowser
		  container_name:  sqlitebrowser
      environment:
	      -  PUID=1000
		    -  PGID=1000
			  -  TZ=Europe/Berlin
			volumes:
			  -  storage:/config
      ports:
        -  3000:3000
      restart:  unless-stopped
  volumes:
    storage:
```