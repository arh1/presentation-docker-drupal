## Docker & Drupal

![Drupal on Docker](slides/img/docker-drupal.png)


### Overview

* Containers for web server, php, db
* But also... Solr, Varnish, Memcache/Redis, logging, mail-handling, etc 
* To date, primarily for local Drupal dev
* Note recommendations from hosts

~Notes:
* e.g. Platform.sh recently recommended Lando
* Major Drupal hosts use containers, but not Docker (afaik)
* Pantheon has been pioneering Drupal container-based infr since before Docker


### Drupal Docker Options

* Docker4Drupal, Lando, Docksal
* Phase2 DevTools
* DDev
* Drupal Docker Initiative
* DrupalVM (Docker version)
* Drupal image from Docker Hub
* Custom Docker compose

~Notes:
* DDI: images & docs on Drupal/Docker best practices
* Range from completely custom to drop in place
* Some discussion about consolidating efforts
