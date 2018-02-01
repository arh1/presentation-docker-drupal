## About Docker

![Drupal on Docker](slides/img/docker-drupal.png)


### What is Docker

* containers !== Docker
* Docker: company & open source tools
* Community Edition vs Enterprise Edition
* < 5

~Notes:
* CE: dev tools
* EE: enterprise prod infr
* docker.com <- Drupal


### Terminology & Concepts

* Dockerfile
* Image / Container
* Service & Microservices
* Docker Compose
* Docker registry
* Volumes

~Notes:
* Dockerfile: Commands to create container
* Image: "blueprint" for container
* Service: ind pieces of app exposed to rest of app via well-defined api
* Service: web server; db server
* Micro arch: app that's a collection of loosely-coupled small services
* Docker handles networking, ports b/w containers
* Registry: formal, versioned storage of images
* Compose: tool for managing multi-container apps
* Volumes: persist data outside containers (down vs stop)


### Installing Docker

* Docker for Mac
* Docker for Windows
* Require recent OS versions
* Mac/Win filesystem performance issues
* Many Linux distros

~Notes:
* Install includes bundle of tools: Docker Engine, Docker CLI client, Docker Compose, Docker Machine, and Kitematic
* Older Mac/Win installs required a VM (Win 10 Pro)
* Mac/Win fs issues being improved currently + workarounds
* Docker sync mitigates for macOS


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
