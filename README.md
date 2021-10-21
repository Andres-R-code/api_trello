# TRELLO REST API

![build status](https://static.pisapapeles.net/uploads/2020/03/Trello-logo-blue.svg.png) 


## _Access to the functions for handling work equipment and assignment of specific tasking.

This API  uses some open-source projects to work properly:

- [Django Rest Framework] - evented I/O for the backend
- [SqlLite] - relational database management system
- [Celery] - asynchronous task project

## Purpose
The purpose of this repository is to demonstrate some techniques for building a REST API using the Django Rest Framework.

## Installation

Requires [Django](https://nodejs.org/) v2.2.24+ to run.

Install the dependencies and devDependencies and start the server.

### Development
```sh
cd api_trello
virtualenv env --no-site-packages
source env/bin/activate
pip install -r requirements.txt
Create a database named Trello CREATE DATABASE Trello;
python manage.py migrate
python manage.py createsuperuser
python manage.py makemigrations ig_miner_app
python manage.py migrate
python manage.py runserver
```

## Plugins

| Plugin | README |
| ------ | ------ |
| Json Web Token | [plugins/jsonwebtoken/README.md][PlJw] |
| Mailtrap | [https://mailtrap.io/][PlBc] |


## Docker

By default, the Docker will expose port 8000, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd api-node
docker build -t <youruser>/api-node .
```

This will create the class center image and pull in the necessary dependencies.


Once done, you need to create a file called **env.list**

```sh
touch env.list
```

write your env vars into the file **env.list**, you might copy them from .env.example 

Finally run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8000 of the Docker (or whatever port was exposed in the Dockerfile):

**Note:** You must run the following command where the env.list file is located

```sh
docker run -d -p 8000:8000 --env-file ./env.list --name=classcenter <youruser>/api-node
```

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
9
   [sequelize]: <https://github.com/sequelize/sequelize/blob/main/README.md>
   [node.js]: <http://nodejs.org>
   [express]: <http://expressjs.com>


