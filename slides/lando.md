![Lando](slides/img/logo-lando.png)

~Notes:
* Very powerful command line: lando


### Install

1. Install Docker
1. Install Lando (installers for Win, Mac)


### App Setup

_To use an existing Drupal codebase_

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

# Logs:
$ lando logs

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

# DB import/export:
$ lando db-import my-db-dump.sql

# Share environment publicly:
$ lando share
</code></pre>


### Debugging


### Pros/Cons

~Notes:
* lando will save you a lot of searching and typing
