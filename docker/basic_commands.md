# About Docker

* Dockerfile (build ->) Docker image
* Docker image (run ->) Docker container


# Basic Commands

* docker build (-t \[image name\]:\(\[tag\]\)) \[dockerfile dir\]: build
* docker image ls, docker images: obtain a list of Docker images
* docker image rm \[image id (obtained by docker images)\]: remove Docker image from device
* docker run -it \[image name\]\(:\[tag\]\): run Docker container from Docker image
  * -it: this option enable us to input in the container
  * --rm: remove container automatically 
* docker ps -a: obtain a list of Docker containers
* docker cp \[container id \(obtained by docker cp -a\)\] \[path to file in container\] \[path to save\]: save the file in the container locally
* docker rm \[container id\]: remove Docker container

