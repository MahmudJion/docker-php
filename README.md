# docker-php
dockerize various PHP frameworks and core PHP files

## PHP
Install and build docker app for your php application

```sh
$ docker build -t my-php-app .
$ docker run -it --rm --name my-running-app my-php-app
```

To run the Apache/php image WITHOUT a dockerfile, run this command:

```sh
$ docker run -d -p 80:80 --name my-apache-php-app -v "$PWD":/var/www/html php:7.2-apache # This line for *nix users
```
Here update your PWD according to your working directory if you are a windows user.

### PHP and docker-compose

```sh
$ docker stop $(docker ps -a -q)
```

Running and Down the docker-composer
```sh
$ docker-compose up -d
$ docker-compose down
```
