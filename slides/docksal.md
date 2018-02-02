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
* Virtualbox VM
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

* Add build steps in `fin init` (bash)
* Addons: custom fin commands (bash)
* Powerful CI service integrations
* Override PHP/MySQL config in .docksal/etc
* Fin app aliases
* `fin share`

~Notes:
* CI: workflows w/ Compose, phpcs, phpunit, Behat, Travis
* Aliases: `fin @myapp stop` from outside app dir


### To the Terminal

~Notes:
* Demo `fin start`
* Demo `fin ps`
* Demo `fin help`
* Demo: show docksal.yml
* Demo: `fin config show` (compiled config)
