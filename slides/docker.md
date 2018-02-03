## About Docker

![Drupal on Docker](slides/img/docker-drupal.png)


### What is Docker

* containers !== Docker
* Docker: company & open source tools
* Community Edition vs Enterprise Edition
* < 5

~Notes:
* Docker evolved from Linux Containers
* CE: dev tools
* EE: enterprise prod infr
* docker.com <- Drupal


### Terminology

* Image / Container
* Docker registry
* Service & Microservices
* Docker Compose
* Stack
* Volumes

~Notes:
* Image: "blueprint" for container
* Registry: versioned image storage
* Service: ind pieces of app exposed to rest of app via well-defined api
* Micro arch: app that's a collection of loosely-coupled small services
* Compose: tool to manage multi-cont apps
* Stack: group of services that work together
* `A stack is a group of interrelated services that share dependencies, and can be orchestrated and scaled together.`
* Volumes: persist data outside containers (down vs stop)


### Installing Docker

* Mac, Windows, Linux distros
* Mac/Win require recent OS versions
* Mac/Win filesystem performance issues

~Notes:
* Install includes bundle of Docker tools
* Older Mac/Win installs required a VM (Win 10 Pro)
* Mac/Win fs issues being improved currently + workarounds (sync, caching)
* @todo: these issues just relevant to volumes?


### Working with Apps in Docker

 <pre><code class="bash" data-trim data-noescape>
# Start an app (in background) based on docker-compose.yml:
$ docker-compose up -d

# List running containers (including names):
$ docker-compose ps

# Check logs:
$ docker-compose logs [CONTAINER_NAME]

# Stop an app:
$ docker-compose stop

# Destroy containers (watch out!):
$ docker-compose down
</code></pre>

~Notes:
* `docker` for lower-level commands; interact with images, build an app
* `docker-compose` to work with app across containers
* `docker-compose up` will pull images if you don't have them yet
* pulling images is the only slow step (but much smaller than VMs)
