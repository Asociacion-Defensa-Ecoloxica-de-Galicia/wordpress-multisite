# ADEGA Wordpress Multisite

## Instructions

Add user to `www-data` group.

```sh
sudo usermod usuario -a -G www-data
newgrp usuario
```
Run containers
```sh
docker-compose up
```
Stop containers
```sh
docker-compose down
```
or 
```sh
Ctrl-C
```