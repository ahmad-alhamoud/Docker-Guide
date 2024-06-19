# Docker-Guide

Docker Guide A comprehensive guide to understanding and using Docker, covering containers, basic commands, Docker architecture, images, Dockerfile, and Docker Compose.

![Docker-Logo-2](https://github.com/ahmad-alhamoud/Docker-Guide/assets/144995844/04ac74cf-c45d-4e68-bef3-1d15e0bf1c4a)


### What is an Image ?
A Docker image is a read-only template with instructions for creating a Docker container. Images are used to package applications and preconfigured server environments.

### What is a Container ?
Lightweight, standalone and executable software package that includes everything needed to run a piece of software.

Containers are designed to provide a consistent and reproducible environment across different platforms and development stages.

Simplifies development, deployment, and scaling.

### Basic Docker Commands

docker pull [image]: Pulls an image or a repository from a registry.

docker run [image]: Runs a command in a new container.

docker ps: Lists all running containers.

docker stop [container_id]: Stops a running container.

docker rm [container_id]: Removes a stopped container.

docker images: Lists all the local images. docker rmi [image_id]: Removes an image from the local repository.

### Docker Architecture

![docker-architecture](https://github.com/ahmad-alhamoud/Docker-Guide/assets/144995844/45d61277-e7df-4778-b522-3fe5a707dfb9)


Docker architecture consists of the following components:

Docker Client: The user interface to Docker. Sends commands to Docker Daemon.

Docker Daemon: Runs on the host machine. Builds, runs, and manages Docker containers.

Docker Images: Read-only templates used to create containers.

Docker Registry: Stores Docker images. Docker Containers: Lightweight, portable encapsulations of an environment in which to run applications.

### Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. It is used to automate the image creation process.

# Here's a basic example of a Dockerfile:

Use an official Python runtime as a parent image
```FROM python:3.8-slim-buster

Set the working directory
WORKDIR /app

Copy the current directory contents into the container at /app
COPY . /app

Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

Make port 80 available to the world outside this container
EXPOSE 80

Define environment variable
ENV NAME World

Run app.py when the container launches
CMD ["python", "app.py"]
```

### Docker Compose File
Docker Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application's services.

Here’s an example of a docker-compose.yml 

![Screenshot (11)](https://github.com/ahmad-alhamoud/Docker-Guide/assets/144995844/78d6932f-2c2b-4206-8fee-05fffeeb9cad)
