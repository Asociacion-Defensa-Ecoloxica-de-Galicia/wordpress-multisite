# ADEGA Wordpress Multisite

## Folders

* `src/` Development folder (/wp-content).
* `config/` Configuration folder for NGINX and Wordpress. 
* `.wp/` Web root folder (/). Excluded from Git repo.
* `logs/` Web server logs. Excluded from Git repo.

## Instructions
Run containers
```console 
$ docker compose up -d
```
Stop containers
```console
$ docker compose down
```