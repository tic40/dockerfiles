
```
$ cd php-docker

# build iamge from Dockerfile
$ docker build -t php56-centos .

# run container from image
$ docker run -it --name php56-centos-container -d -p 8080:8080 php56-centos

# login to the container
$ docker exec -it php56-centos-container bin/zsh
```
