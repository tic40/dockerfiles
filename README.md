# dockerfiles

## OVERVIEW

this is a repository to be stored my docker files

## BASIC USAGE

### DOCKERFILE
```
# build
$ cd {directory}
$ docker build -t {image-name} .
```

```
# run
$ docker run -it --name {container-name} {image-name}
```

```
# create volume
$ docker run -it --name {container-name} -v {local-path}:{container-path} {image-name}
```

### DOCKER-COMPOSE
```
$ cd {directory}
$ docker-compose up
```
