## History

![Drupal on Docker](slides/img/docker-drupal.png)


### Bare Metal

* Local servers, e.g. MAMP, WAMP, XAMPP, custom
* Hard to manage multiple versions
* Hard to synch with prod
* Can't share with other devs
* "Works for me"

~Notes:

* 


### Virtualization

* Virtual machines, e.g. Drupal VM, Acquia Dev Desktop, custom
* Mononlithic
* Lots of disk, memory
* Maintenance is hard
* Big files and slow to provision
* Hard to share

~Notes:

* 


### Containers: Why

* Fast
* Easier to maintain than VMs
* Easy to share with other devs
* Easy to duplicate across locals, stage, prod
* Flexibility & modularity


### Containers: What

```A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings.```


### Containers: What

* Like a VM, but all containers on a host share the same OS
* Each container runs as its own process on the host


### Containers: How

![VM architecture](slides/img/docker.com-VM@2x.png)
![container architecture](slides/img/docker.com-Container@2x.png)

~Notes:

* 