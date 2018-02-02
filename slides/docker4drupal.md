## Docker4Drupal

![Wodby](slides/img/logo-wodby.png)


### Overview

* Docker-based application hosting + infrastructure management service
* You provide server (e.g. AWS acct) and repo
* Wodby handles management + deployment via dashboard
* Local dev options are bare bones Docker/Drupal approach by Wodby
* Essentially a nice compose file that's tuned for Drupal
* "Stacks" for deploying to prod

~Notes:
* @todo: less words

### Install

* Just install Docker!


### App Setup

1. Create your Drupal codebase
1. Download Docker4Drupal's docker-compose.yml
1. Compose file: Uncomment an image, change some paths 
1. Set db credentials in settings.php
1. Edit /etc/hosts to configure domains
1. <pre><code class="bash" data-trim data-noescape>docker-compose up -d</code></pre>
1. Site up at http://drupal.docker.localhost:8000

~Notes:
* Default d4d image has PHP+Drupal
* Show docker-compose.yml
* @todo: list default images


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start/stop:
$ docker-compose up -d
$ docker-compose stop

# Execute command in 'php' container:
$ docker-compose exec --user 82 php pwd

# Drop into shell in 'php' container:
$ docker-compose exec --user 82 php /bin/bash

# Logs from 'php' container:
$ docker-compose logs php

# Add/change a service:
# Uncomment/add entry to 'services' key in docker-compose.yml
</code></pre>

~Notes:
* @todo: when do we see a compose file? (we reference edits here)
* 82 is default uid/gid for www-data user on Alpine Linux (otherwise root)


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Drush, Console, Composer:
$ docker-compose exec --user 82 php drush status -r
  /var/www/html/web
$ docker-compose exec --user 82 php drupal list
$ docker-compose exec --user 82 php composer list

# Execute PHP:
$ docker-compose exec --user 82 php php -r 'echo "foo\n";'

# MySQL shell:
$ docker-compose exec mariadb /usr/bin/mysql -uroot
  -p"password"

# DB Import: Add my-db-dump.sql to a specific dir, uncomment a line
# in compose file

# DB export:
$ docker-compose exec mariadb sh -c 'exec mysqldump -uroot
  -p"password" my-db' > my-db.sql

# Add/change a service:
# 
</code></pre>

~Notes:
* @todo: couldn't we import db using /usr/bin/mysql?


### Extras

* Deploy to Wodby!
* Lots of Drupal-focused images


### To the Terminal

~Notes:
* Demo: `docker-compose up -d`
* Demo: show docker-compose.yml
