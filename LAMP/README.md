# LAMP Stack in Docker
## Build Docker images
```
$ sudo docker-compose build
```


## Create '/var/www/html' web volume
Create a local volume that can be mounted within docker


```
$ sudo docker volume create --driver local \
    --opt type=none \
    --opt device=~/web/www/html \
    --opt o=bind www-volume
```


## Create MariaDB Volume
We will also need a MariaDB Volume

```
$ sudo docker volume create --driver local \
    --opt type=none \
    --opt device=~/web/db/mysql \
    --opt o=bind mariadb-volume
```