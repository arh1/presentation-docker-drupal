![Lando](slides/img/logo-lando.png)


### Overview

* By Tandem
* Still in beta
* `lando`
* Docker abstractions
* Extensible
* D6, D7, D8, Backdrop, WP, MEAN, .NET ...

~Notes:
* Next gen Kalabox
* Beta, heavy development, upgrade warnings
* Abstracts Docker concepts -- concise config
* .lando.yml -- simple or very complex


### Install

1. Install Docker
1. Run Lando installer (for Win, Mac) or download package (Linux)


### App Setup

1. Create your Drupal codebase
1. `lando init` or create .lando.yml
1. Optional: Select a recipe via `lando init --recipe drupal8`
1. Optional: Specify your codebase repo via `lando init github`
1. <pre><code class="bash" data-trim data-noescape>lando start</code></pre>
1. Site available at http://myproject.lndo.site/

~Notes:
* .lando.yml: abstracted compose file + landoisms
* Create codebase or `lando init github|pantheon`
* 'recipe': D Stack + Lando extensions
* Services (default & D8): just appserver & db
* .lando.yml 'services' key: abstraction of docker compose format


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start/stop:
$ lando start
$ lando stop

# Execute command in container:
$ lando ssh appserver -c "pwd"

# Drop into shell in 'appserver' container:
$ lando ssh appserver

# Logs from 'appserver' container:
$ lando logs appserver

# Add/change a service:
# Add entry to 'services' key in .lando.yml
</code></pre>

~Notes:
* no `lando exec`
* Services: Add to 'services' key & `lando rebuild`


### Working with Apps

<pre><code class="bash" data-trim data-noescape>
# Drush, Console, Composer:
$ lando drush status
$ lando drupal list
$ lando composer list

# Execute PHP:
$ lando php -r 'echo "foo\n";'

# MySQL shell:
$ lando mysql

# DB import/export:
$ lando db-import my-db-dump.sql
$ lando db-export
</code></pre>


### Extras

* Drop-in additional services
* Pre-made recipes
* Build steps
* Events framework
* Pre-run scripts
* Tool integrations
* Tooling: alias commands inside containers
* Advanced plugin system & API
* `lando share`

~Notes:
* Build step: e.g. `composer install` on app re/start
* Events: e.g. `drush cr` after post-db-import event
* Pre-run: /scripts before booting each container
* Tooling: alias `lando mycommand`
* Tools: e.g. phpcs, phpunit, Behat, Travis
* Share: localtunnel


### To the Terminal

~Notes:
* Demo: show .lando.yml
* Demo `lando start`
* Demo `lando info`
* Demo `lando` (help)
