## About Docker

![Drupal on Docker](slides/img/docker-drupal.png)


### What is Docker

* Docker !== containers
* Docker is a company, and open source toolset
* Docker CE (dev tools) vs Docker EE (enterprise prod infrastructure)
* Docker isn't 5 yet
* docker.com <- Drupal

~Notes:
* 


### Terminology & Concepts

* Dockerfile: commands to create a container
* Docker Image:
* Docker Compose: 
* Docker Engine: 
* Docker registry: 
* Orchestration: 
* Docker CLI: 
* Docker Machine: 
* Volumes

~Notes:
* 


### Installing Docker

* Mac, Windows, many Linux distros
* Windows requires Win 10 Professional
* Docker for Mac/Win installs a very small VM
* MacOS/Win file system performance issues

~Notes:
* Install includes: Docker Engine, Docker CLI client, Docker Compose, Docker Machine, and Kitematic
* Mac/Win fs issues being improved currently + workarounds
* Docker sync mitigates for MacOS


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
* docker-compose up will pull images if you don't have them yet
* docker-compose to work with multi-container apps
* docker for lower-level commands; interact with images, build an app
