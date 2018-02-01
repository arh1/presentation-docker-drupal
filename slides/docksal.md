![Docksal](slides/img/logo-docksal.png)

## FFW


### Overview

* Formerly Drude/DDE
* Local dev env toolset by FFW
* (For now) uses a thin VirtualBox VM across all projects 

~Notes:
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
* `fin config generate` creates compose file docksal.yml


### Working with Apps

 <pre><code class="bash" data-trim data-noescape>
# Start (VM and containers:
$ fin start

# Execute command in 'cli' container:
$ fin exec pwd

# Drop into shell in 'cli' container:
$ fin bash cli

# Logs:
$ fin logs cli

# Stop:
$ fin stop
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

# Add/change a service:
# Add/change image value in docksal.yml
</code></pre>

~Notes:
* Demo `fin start`
* Demo `fin help`


### Extras

* Add build steps in `fin init` (bash)
* Addons: custom fin commands (bash)
* Share environment publicly: `fin share`


~Notes:
* 
