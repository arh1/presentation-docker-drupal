## Docker4Drupal

![Wodby](slides/img/logo-wodby.png)

~Notes:
* Docker-based application hosting + infrastructure management service
* You provide server (e.g. AWS acct) and repo
* Wodby handles management + deployment via dashboard
* Local dev options are bare bones Docker/Drupal approach by Wodby
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

# SSH into 'php' container:
$ 

# Logs from 'php' container:
$ docker-compose logs --user 82 php

# Stop:
$ docker-compose stop
</code></pre>


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Drush, Console, Composer:
$ docker-compose exec --user 82 php drush status
$ docker-compose exec --user 82 php drupal list
$ 

# Execute PHP:
$ lando php -r 'echo "foo\n";'

# MySQL shell:
$ lando mysql

# DB import/export:
$ 

# Share environment publicly:
$ 
</code></pre>


### Debugging


### Pros/Cons

* 

~Notes:
* 
