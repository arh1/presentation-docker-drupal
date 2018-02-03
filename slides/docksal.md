![Docksal](slides/img/logo-docksal.png)


### Overview

* By FFW
* `fin`
* Docker abstractions
* Uses a VM across all projects
* Focused on Drupal & WP

~Notes:
* Formerly Drude (DDE)
* Docker config in .docksal: none to simple to complex
* Virtualbox VM (to be deprecated)
* VM mitigates filesystem performance issues (Mac)
* And networking issues (Win)
* VM runs boot2docker tiny distro


### Install

1. Install Docker
1. Win: install Babun shell
1. Linux: fix port conflicts w/ bare metal servers
1. Run Docksal installer

~Notes:
* Babun to be deprecated in favor of WSL


### App Setup

1. Create your Drupal codebase
1. Create .docksal dir
1. Optional: specify non-default stack (e.g. Acquia)
1. Optional: generate compose file for manual config
1. <pre><code class="bash" data-trim data-noescape>fin start</code></pre>
1. Site available at http://myproject.docksal/

~Notes:
* Just .docksal dir for default stack
* Specify stack in docksal.env
* Generate docksal.yml -- Compose file -- to customize
* `fin config generate` creates compose file docksal.yml
* Services: db (MySQL), cli (php-fpm), web (Apache) (+ SSH, DNS, reverse proxy)


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start (VM and containers):
$ fin start
$ fin stop

# Execute command in 'cli' container:
$ fin exec pwd

# Drop into shell in 'cli' container:
$ fin bash cli

# Logs:
$ fin logs cli

# Add/change a service:
# Add entry to 'services' key in .docksal/docksal.yml
</code></pre>


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Drush, Console, Composer:
$ fin drush status
$ fin drupal list
$ fin exec composer list

# Execute PHP:
$ fin exec php -r 'echo "foo\n";'

# MySQL shell:
$ fin db cli

# DB import/export:
$ fin db import my-db-dump.sql
$ fin db dump my-db-dump.sql
</code></pre>


### Extras

* Drop-in additional services
* Acquia stack
* Easily override PHP/MySQL config
* Tool integrations
* Custom `fin` commands
* Fin app aliases
* `fin share`

~Notes:
* Services: solr, memcache, etc
* PHP/MySQL config: .docksal/etc
* Tools: e.g. Behat, phpcs, sass/compass
* Aliases: `fin @myapp stop` from outside app dir
* Share: via ngrok


### To the Terminal

~Notes:
* Demo `fin start` (VM already running)
* Demo `fin ps`
* Demo `fin help`
* Demo: show docksal.yml
* Demo: `fin config show` (compiled config)
