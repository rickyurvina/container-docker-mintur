# Docker

This template has been designed to meet the following requirements:

A backend container with official dockerhub image php: 7.4-fpm PHP version 7.4 and Supervisor with php command artisan queue: work

A frontend container with the official dockerhub node image: latest and angular CLI

A mysql container with official mysql: latest dockerhub image

A phpmyadmin container with the official dockerhub image phpmyadmin / phpmyadmin, linked to the mysql container in order to access the DB

A webserver container with the official image of the dockerhub nginx: alpine

## Init Docker


The /docker/backend/supervisor/supervisord.conf file is linked in the backend container. Editing that file is instantly replicated to the container

First installation

Proceed with the copy of the .env.example file for setting the project and user name to be created for DB mysql

`cp .env.example .env`

Wait for everything to be configured

Then:

`docker-compose up -d`

Once all the containers are initialized, you need to connect to the backend container:

`docker exec -t -i backend / bin / bash`


backend: `localhost:8000`

frontend: `localhost:80`

phpmyadmin: `localhost:7000`




