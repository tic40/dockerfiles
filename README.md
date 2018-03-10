# dockerfiles

## OVERVIEW

this is a repository to be stored my docker files

## BASIC USAGE

### DOCKER COMPOSE

```sh
# build and start
$ docker-compose up

# start
$ docker-compose start
# stop
$ docker-compose stop

# build
$ docker-compose build
```

### DOCKERFILE
```sh
# build
$ docker build -t {image-name} .
```

```
# run
$ docker run -it --name {container-name} {image-name}
```

```
# create volume
$ docker run -it --name {container-name} -v {local-path}:{container-path} {image-name}

# login
$ docker exec -it {container-name} /bin/bash
```
