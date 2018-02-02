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
1. Create .lando.yml file or initialize with `lando init`
1. Optional: Select a recipe via `lando init --recipe drupal8`
1. <pre><code class="bash" data-trim data-noescape>lando start</code></pre>
1. Site available at http://myproject.lndo.site/

~Notes:
* .lando.yml is all that's required
* Create codebase, or `init` with Pantheon or Github method
* Lando 'recipe' is a Docker stack plus Lando extensions
* Default (and D8) stack: just appserver and db services
* 'services' key in .lando.yml is abstraction of docker compose format


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start/stop:
$ lando start
$ lando stop

# Execute command in container:
# Use a more specific lando command, or SSH in

# Drop into shell in 'appserver' container:
$ lando ssh appserver

# Logs from 'appserver' container:
$ lando logs appserver

# Add/change a service:
# Add entry to 'services' key in .lando.yml
</code></pre>

~Notes:
* Add to 'services' and run `lando rebuild`


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

~Notes:
* Demo: show .lando.yml
* Demo `lando start`
* Demo `lando info`
* Demo `lando help`


### Extras

* Pre-built recipes & services
* Build steps
* Events framework
* Pre-run scripts
* Tooling: custom lando commands (yaml)
* Powerful CI service integrations/docs
* `lando share`
* Advanced plugin system & API

~Notes:
* Build step: e.g. run `composer install` on every app start/restart
* Events: e.g. run `drush cr` after post-db-import event
* Pre-run: execute bash scripts in /scripts before booting each container
* Tooling: alias `lando mycommand` for commands inside containers
* CI: workflows w/ Compose, phpcs, phpunit, Behat, Travis
* Share: uses localtunnel
