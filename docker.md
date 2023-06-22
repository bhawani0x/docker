# Docker
Docker is a containrized application tools & in this tools are using light weight images for deploy, build and running. Docker is an open platform for developing, shipping, and running applications.

# What is Dockerfile:
- A Dockerfile is a text file that contains a series of commands or instructions.
- These instructions are executed in the order in which they are written.
- Execution of these instructions takes place on a base image.
- You will use a Dockerfile to create your own custom Docker image

# Docker File Components

## FROM
The `FROM` command specifies the base image for the Docker image. It should be placed at the top of the Dockerfile.

## RUN
The `RUN` command is used to execute a command in the Docker image during the build process. It creates a new layer in the image.

## MAINTAINER
The `MAINTAINER` command specifies the author, owner, or description of the Docker image.

## COPY
The `COPY` command copies files from the local system (Docker VM) to the Docker image. You need to provide the source and destination paths.

## ADD
The `ADD` command is similar to `COPY`, but it also provides the ability to download files from the internet and extract files at the Docker image side.

## EXPOSE
The `EXPOSE` command is used to specify which ports should be exposed by the Docker image, such as port 8080 for Tomcat or port 80 for Nginx. It informs Docker that the container listens on the specified network ports at runtime.

## WORKDIR
The `WORKDIR` command sets the working directory for the Docker container. It allows you to specify the directory where subsequent commands will be executed within the container.

## CMD
The `CMD` command specifies the default command to be executed when the Docker container is created. It is typically used for defining the main process or command that runs within the container. Only the last `CMD` instruction in the Dockerfile is effective.

## ENTRYPOINT
The `ENTRYPOINT` command is similar to `CMD`, but it has higher priority. The commands specified by `ENTRYPOINT` will be executed first. It provides an entry point for running the container and allows you to configure a container that can be run as an executable.

## ENV
The `ENV` command is used to set environment variables within the Docker image. It allows you to define variables that can be accessed by processes running inside the container.

# Docker Commands

### Check Docker Version
```
docker --version
```
Checks the Docker version.

### Install Docker
```
yum install docker -y
```
Installs Docker (for Linux-based systems).

### Start Docker Service
```
systemctl start docker
```
Starts the Docker service.

### Enable Docker on Boot
```
systemctl enable docker
```
Enables Docker to start on system boot.

### List Running Containers
```
docker container ls
```
Lists only the running containers.

### List All Containers
```
docker container ls -a
```
Lists all containers, including stopped ones.

### List Docker Images
```
docker images ls
```
Lists Docker images.

### Create and Deploy a Container
```
docker container run <image id>
```
Creates a container from an image and deploys it.

### Create and Run a Container with Command
```
docker container run <image id> <command>
```
Creates a container from an image and specifies a command to run.

### Create and Run a Detached Container with Command
```
docker container run -d <image id> <command>
```
Creates a container from an image, runs it in detached mode, and specifies a command to run.

### Create and Run an Interactive Detached Container
```
docker container run -d -it <image id>
```
Creates a container from an image, runs it in detached mode with an interactive terminal.

### Stop a Running Container
```
docker container stop <container id>
```
Stops a running container.

### Start a Stopped Container
```
docker container start <container id>
```
Starts a stopped container.

### Pull Image from Docker Hub
```
docker pull <image name>
```
Pulls an image from Docker Hub.

### Remove a Container
```
docker container rm <container id>
```
Removes a container.

### Remove a Container Forcefully
```
docker container rm <container id> -f
```
Removes a container forcefully.

### Access a Running Container
```
docker exec -it <container id> bash
```
Accesses a running container and opens a bash shell.

### Inspect Container
```
docker container inspect <container id>
```
Inspects a container to retrieve information, including its IP address.

###

 Remove Docker Image
```
docker rmi <image id>
```
Removes a Docker image.

### Check Container RAM Usage
```
docker container stats <id>
```
Checks the RAM usage of a container.

### Rename a Container
```
docker container rename <container id> <new name>
```
Renames a container.

### Create a New Container with a Specific Name
```
docker container run -d -it --name <new name> <image name>
```
Creates a new container with a specific name.

### Forcefully Stop a Running Container
```
docker container kill <container id>
```
Forcefully stops a running container.

### Export Container as Tar File
```
docker container export <container id> > <name.tar>
```
Exports a container as a tar file for transferring to another server.

### Build Docker Image from Dockerfile
```
docker build -t <image name> .
```
Builds a Docker image using a Dockerfile in the current directory.

Feel free to adjust the formatting or add more details as needed for your specific requirements.
