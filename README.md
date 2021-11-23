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

## Codeigniter 3

From the command prompt run the following command. Make sure you are in the project folder.

```sh
$ docker-compose up -d
```

## Codeigniter 4

Build the image:

```sh
$ docker build . -t codeigniter:4.1.5
```

Start the container:

```sh
$ docker container run -it --publish 80:80 --name ci4 -v /localfolder:/var/www/html codeigniter:4.1.5
```

### With Docker Composer

From your project directory, start up your application by running:

```sh
$ docker-compose up -d
```

From your project directory, stop your application by running:

```sh
$ docker-compose down --volumes
```

## Laravel

Build your Dockerfile

```sh
$ docker build -t my_app .
```
Then, we may need to see the Image ID using this command.

```sh
$ docker image ls
```
Copy the image ID from the lists, and then we can run the image.

```sh
$ docker run -p 8000:8000 -d <imageID>
```
Then, we can get access to its command line using this command:

```sh
$ docker exec -it <container ID> sh
```

Inside the container command line, we can start the server using the usual

```sh
php artisan serve
```

### Running the Image with Docker Compose

For running the app, we can easily type this command

```sh
$ docker-compose up
```