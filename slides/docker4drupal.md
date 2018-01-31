## Docker4Drupal

![Wodby](slides/img/logo-wodby.png)

~Notes:
* Docker-based application hosting + infrastructure management service
* You provide server (e.g. AWS acct) and repo
* Wodby handles management + deployment via dashboard
* Local dev options are bare bones Docker/Drupal approach by Wodby
* Essentially a nice compose file that's tuned for Drupal
* "Stacks" for deploying to prod


### Install

* Just install Docker!


### App Setup

_To use an existing Drupal codebase_

1. Download Docker4Drupal's docker-compose.yml
1. docker-compose.yml: Uncomment an image, change some paths 
1. Set db credentials in settings.php
1. Edit /etc/hosts to configure domains
1. <pre><code class="bash" data-trim data-noescape>docker-compose up -d</code></pre>
1. Site up at http://drupal.docker.localhost:8000

~Notes:
* Default d4d image has PHP+Drupal
* Show docker-compose.yml


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start:
$ docker-compose up -d

# Execute command in 'php' container:
$ docker-compose exec --user 82 php ls

# Execute shell in ("SSH into") 'php' container:
$ docker-compose exec --user 82 php /bin/bash

# Logs from 'php' container:
$ docker-compose logs php

# Stop:
$ docker-compose stop
</code></pre>

~Notes:
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

# DB Import: Create a dir, add db dumps, uncomment a line
# in compose file

# DB export:
$ docker-compose exec mariadb sh -c 'exec mysqldump -uroot
  -p"password" my-db' > my-db.sql

# Share environment publicly:
$ 
</code></pre>


### Debugging

1. Set ```PHP_XDEBUG: 1``` and ```PHP_XDEBUG_DEFAULT_ENABLE: 1``` in compose file
1. A couple of additional networking steps for macOS and Win
1. Configure your IDE to use Xdebug
1. Start debugging session


### Pros/Cons

* 

~Notes:
* 
