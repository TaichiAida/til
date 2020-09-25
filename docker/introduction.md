# Docker
Today I used docker for the first time.  
I just made **Dockerfile** to join a container.  

## Dockerfile
I made C++ environment in ubuntu 18.04.  
```
# ./Dockerfile
# image
FROM ubuntu:18.04

# get cpp
RUN apt-get update && \
    apt-get install -y build-essential cmake clang libssl-dev vim

# run unix command, mkdir
RUN mkdir work

# copy dir
COPY ./src/ work/src/
COPY README.md work/

# define initial dir
WORKDIR work
```

## Build Dockerfile
To make Images, build dockerfile.  
```
$ docker build --rm -f Dockerfile -t ubuntu:18.04 .
```

Check the image
```
$ docker images
> REPOSITORY    TAG    ...
> ubuntu        18.04  ...
```

## Run Image
```
$ docker run --rm -it ubuntu:18.04

> work/:$
```

