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
