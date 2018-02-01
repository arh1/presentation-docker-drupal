## Wrapping Up

![Drupal on Docker](slides/img/docker-drupal.png)


### Recap

* Docker is ready now for your local Drupal dev!

~Notes:
* 


### Comparing Toolsets: Docker4Drupal

* Wired for Wodby
* Good for learning Docker
* Familiar for non-Drupal devs
* Starting point for customization
* A little more setup work
* A little more local workflow friction


### Comparing Toolsets: Lando

* ```lando``` command rocks
* Nice integration with app management & CI tools
* No compose file

~Notes:
* lando cli will save you a lot of searching and typing
* lando services dynamically create Docker compose object
* .lando.yml rather than docker-compose.yml (by default)
* can't run docker-compose commands


### Comparing Toolsets: Docksal

* ```fin``` command rocks
* Requires VirtualBox
* Slower startup with VM
* Slightly better filesystem performance (anecdotal) on macOS, Win
* Nice integration with app management & CI tools
* No compose file


### Discussion


### Credits

* reveal.js: https://github.com/hakimel/reveal.js
* Drupal/Docker image: https://hub.docker.com/r/paolomainardi/docker-drupal-cli-extra/ ![Drupal on Docker](slides/img/docker-drupal.png)

~Notes:
* 


### Links

* Docker4Drupal: https://wodby.com/stacks/drupal/docs/local/; https://github.com/wodby/docker4drupal
* Lando: https://docs.devwithlando.io/; https://github.com/lando/lando
* Dockal: https://docksal.io/; https://github.com/docksal/docksal
* Docker: https://www.docker.com/
* Docker Hub: https://hub.docker.com/

~Notes:
* 
