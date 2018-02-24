
```
$ cd rails-centos-docker

# build iamge from Dockerfile
$ docker build -t rails-centos .

# run container from image
$ docker run -it --name rails-centos-container -d -p 3000:3000 rails-centos

# login to the container
$ docker exec -it rails-centos-container bin/zsh
```
