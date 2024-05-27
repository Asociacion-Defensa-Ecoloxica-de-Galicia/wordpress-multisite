# ADEGA Wordpress Multisite

## Folders

* `src/` Development folder (/wp-content).
* `config/` Configuration folder for NGINX and Wordpress. 
* `doc` Documentation related files.
* `.wp/` Web root folder (/). Excluded from Git repo.
* `.db/` Database files. Excluded from Git repo.
* `logs/` Web server logs. Excluded from Git repo.

## Environment
### Installation
* Prerequisites:
    * Git
    * Docker
* Clone repository to your develop folder:
```console
git clone https://github.com/Asociacion-Defensa-Ecoloxica-de-Galicia/wordpress-multisite.git
```
### Using environment
* Run containers.
```console 
$ docker compose up -d
```
* Access Wordpress at http://localhost:8080.
* Stop containers.
```console
$ docker compose down
```
## Setting up Wordpress

### Basic setup

Open Wordpress and follow dialogs.

![Select languaje](doc/images/img01.png)
![Provide site data](doc/images/img02.png)
![Click to login](doc/images/img03.png)
![Login](doc/images/img04.png)

### Setting up WP multisite
1. Enable Multisite.

![Go to network initialization](doc/images/img11.png)
![Select using paths for network sites](doc/images/img12.png)

2. Uncomment `config/wp/wp-config.php` multisite lines and save.

![Uncomment multisite config lines](doc/images/img13.png)

3. Login again.

![Go to login page](doc/images/img14.png)

4. Go to `sites` WP pannel.

![Go to sites pannel](doc/images/img21.png)

## Managing network sites

### Create new site.

1. Create the site.

![Click add new site button](doc/images/img22.png)
![Provide new site data](doc/images/img23.png)

2. Go to new site pannel.

![Go to new site pannel](doc/images/img24.png)

### Managing multisite themes and plugins

WP network sites can only use the themes and plugins previously authorized by the network admins. You can authorize themes and plugins installing them by `nerwork administrator` pannel.

1. Go to network plugins or themes pannel.

![Go to network administrator menu](doc/images/img41.png)

2. Search and install the desired plugin or theme.

![Install new plugin or theme](doc/images/img42.png)

3. ONLY FOR THEMES: enable theme for network so it becomes available for all the network sites.

![If it's a theme, enable it for network sites](doc/images/img43.png)

4. Now you can apply the installed theme or enable the installed plugin for any site opening correspondig site pannel.