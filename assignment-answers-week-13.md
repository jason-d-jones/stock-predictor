## What does it mean to create a Docker image and why do we use Docker images?

A Docker image is a fixed executable file containing everything needed to run the application including, but not limited to, software, libraries, and configuration files.

## Please explain what is the difference from a Container vs a Virtual Machine?

A virtual machine contains an entire operating system that can be run on a host machine. A Docker container contains a much more limited set of software. Virtual machines are isolated from eachother and duplicate all functionality, while Docker container's can share the same OS kernel with other containers. This means that the marginal cost in computational resources for each additional Docker container is less than the initial container. Docker containers can also be started much more quickly than booting up a VM.

## What are 5 examples of container orchestration tools (please list tools)?  

Kubernetes, Docker Swarm, Openshift, Rancher and Nomad.

## How does a Docker image differ from a Docker container?

Docker containers are instances of a Docker image that have been executed. Docker containers are mutable and have a persistant state. 
