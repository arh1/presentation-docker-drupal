![Lando](slides/img/logo-lando.png)

## Tandem

~Notes:
* Very powerful command line: lando


### Install

1. Install Docker
1. Run Lando installer (for Win, Mac) or download package (Linux)


### App Setup

1. Create your Drupal codebase
1. Initialize your project with ```lando init``` or manually
1. Select a recipe during init
1. <pre><code class="bash" data-trim data-noescape>lando start</code></pre>
1. Site available at http://yourproject.lndo.site/

~Notes:
* Lando 'recipe' is a Docker stack


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start:
$ lando start

# Execute command in container:
# Use a more specific lando command, or SSH in

# SSH into 'appserver' container:
$ lando ssh appserver

# Logs from 'appserver' container:
$ lando logs appserver

# Stop:
$ lando poweroff
</code></pre>


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

# Share environment publicly:
$ lando share
</code></pre>


### Extras

* Add build step in .lando.yml, run during ```lando start```
* Nice integration with Composer, phpunit, phpcs 
* Nice integratio docs w/ CI tools
* Tooling: custom lando commands

~Notes:
* With build step, 'lando start' will initialize/update entire app
