
```
$ cd rails-docker

# build iamge from Dockerfile
$ docker build -t rails .

# run container from image
$ docker run -it --name rails-container -d -p 3000:3000 rails

# login to the container
$ docker exec -it rails-container bin/zsh
```
