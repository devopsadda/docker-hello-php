# docker-hello-php
Build a docker image using a simple PHP Hello-World Application and run as a container (containerization php application)

## Step 01: Get Your application ready
```bash
$ mkdir docker-hello-world
$ cd docker-hello-world
$ mkdir src
$ cd src

$ vim index.php
```
```php
<?php

echo "Hello World ...!!!<br/>";
echo "I have successfully containerized my php application!!!";

?>
```
## Step02: Write Dockerfile for your application
```bash
$ cd ..
$ pwd
/home/cloud_user/docker-hello-php
$ vim Dockerfile
```
```bash
FROM php:7.2-apache

COPY src/ /var/www/html/

EXPOSE 80
```
## Step03: Build Docker Image
```bash
$ docker build -t tanvir0102/php-hello-world .
```
## Step04: Run as Docker container and Test your application
```bash
$ docker image ls
$ docker run -d -p 80:80 --name hello-php-app tanvir0102/php-hello-world
$ curl http://localhost:80
```
## Step05: Push the image to Docker Hub Registry
```bash
$ docker login
$ docker push tanvir0102/php-hello-world
```
## Step06: Do cleanup and pull your image from dockerhub and run as container
```bash
$ docker container ls
$ docker container stop hello-php-app
$ docker container rm hello-php-app
$ docker image ls
$ docker image rm tanvir0102/php-hello-world
$ docker run -d -p 80:80 --name hello-php-app tanvir0102/php-hello-world
$ curl http://localhost:80
$ docker image ls
$ docker container ls
```
