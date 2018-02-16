
```
$ cd rails-docker

# build iamge from Dockerfile
$ docker build -t rbenv .

# run container from image
$ docker run -it --name rbenv-container -d -p 3000:3000 rbenv

# login to the container
$ docker exec -it rbenv-container bin/zsh
```
