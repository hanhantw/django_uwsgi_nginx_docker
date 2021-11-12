# django_uwsgi_nginx_docker

Build a diango project with nginx and uwsgi on Docker

## Project structure (with default files)

.
+-- app
|   +-- requirement.txt
+-- nginx
|   +-- sites
|   |   +-- {site}.conf
|   +-- Dockerfile
|   +-- nginx.conf
+-- log
+-- .env
+-- docker-compose.yml
+-- Dockerfile

## Depoly

```shell
docker-compose run web django-admin startproject main .
```
