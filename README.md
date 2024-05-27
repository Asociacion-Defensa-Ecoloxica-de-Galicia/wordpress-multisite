# ADEGA Wordpress Multisite

## Folders

* `src/` Development folder (/wp-content).
* `config/` Configuration folder for NGINX and Wordpress. 
* `.wp/` Web root folder (/). Excluded from Git repo.
* `.db/` Database files. Excluded from Git repo.
* `logs/` Web server logs. Excluded from Git repo.

## Instructions
### Installing environment
* Prerequisites:
    * Git
    * Docker
* Clone repository to your develop folder:
```console
git clone https://github.com/Asociacion-Defensa-Ecoloxica-de-Galicia/wordpress-multisite.git
```
### Using environment
Run containers
```console 
$ docker compose up -d
```
Stop containers
```console
$ docker compose down
```

### Using WP multisite
1. Enable Multisite.

![Go to network initialization](doc/images/img11.png)
![Select using paths for network sites](doc/images/img12.png)

2. Uncomment `config/wp/wp-config.php` multisite lines and save.

![Uncomment multisite config lines](doc/images/img13.png)

3. Login again.

![Go to login page](doc/images/img14.png)

4. Go to `sites` WP pannel.

![Go to sites pannel](doc/images/img21.png)

5. Create new site.

![Click add new site button](doc/images/img22.png)
![Provide new site data](doc/images/img23.png)

6. Go to new site pannel.

![Go to new site pannel](doc/images/img24.png)

### Managing multisite themes and plugins

WP network sites can only use the themes and plugins previously authorized by the network admins. You can authorize themes and plugins installing them by `nerwork administrator` pannel.

![Go to network administrator menu](doc/images/img41.png)
![Install new plugin or theme](doc/images/img42.png)