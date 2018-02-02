## Docker & Drupal

![Drupal on Docker](slides/img/docker-drupal.png)


### Overview

* Images for web server, php, db
* But also... Solr, Varnish, Memcache/Redis, logging, mail-handling, etc 
* To date, primarily for local Drupal dev
* Note recommendations from hosts

~Notes:
* e.g. Platform.sh recently recommended Lando
* @todo: containers in heavy use by prod hosts, just not Docker, right?


### Debugging

1. Enable Xdebug for PHP in compose file
1. Configure your IDE to use Xdebug
1. Start debugging session

~Notes:
* @todo: remove?
* Generally the same across toolsets
* Toolset handles ports and networking
* Might be add'l networking steps for macOS and Win


### Drupal Docker Options

* Docker4Drupal, Lando, Docksal
* Phase2 DevTools
* DDev
* Drupal Docker Initiative
* DrupalVM (Docker version)
* Drupal image from Docker Hub
* Custom Docker compose

~Notes:
* @todo: what is DDI?
* Range from completely custom to drop in place
* Some discussion about consolidating efforts
