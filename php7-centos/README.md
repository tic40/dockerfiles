
```
$ cd php-docker

# build iamge from Dockerfile
$ docker build -t php7-centos .

# run container from image
$ docker run -it --name php7-centos-container -d -p 8080:8080 php7-centos

# login to the container
$ docker exec -it php7-centos-container bin/zsh
```
