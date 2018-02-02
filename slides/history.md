## History

![Drupal on Docker](slides/img/docker-drupal.png)


### Bare Metal

* Local servers, e.g. MAMP, WAMP, XAMPP, custom
* Hard to manage multiple versions
* Hard to synch with prod
* Can't share with other devs
* "Works for me"


### Virtualization

* Virtual machines, e.g. Drupal VM, Acquia Dev Desktop, custom
* Mononlithic
* Lots of disk, memory
* Maintenance is hard
* Big files, slow to provision


### Containers: Why

* Fast
* Easier to maintain than VMs
* Easy to share with other devs
* Easy to duplicate across locals, stage, prod
* Flexibility & modularity


### Containers: What

`Linux containers are self-contained execution environments... that share the kernel of the host operating system.`
--Infoworld

~Notes:
* `The result is something that feels like a virtual machine, but sheds all the weight and startup overhead of a guest operating system.`
* `Containers decouple applications from operating systems`


### Containers: What

* Like VMs, but all containers share OS
* Each container runs as its own process on the host
* Microservices


### Containers: How

![VM architecture](slides/img/docker.com-VM@2x.png)
![container architecture](slides/img/docker.com-Container@2x.png)
