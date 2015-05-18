# Provision Azure Boxes With Vagrant

This repository contains the playbook discussed in my article [Provision Azure Boxes With Vagrant](http://unindented.org/articles/provision-azure-boxes-with-vagrant/).

Install [VirtualBox](https://www.virtualbox.org/), [Vagrant](https://www.vagrantup.com/) and the [Vagrant Azure Provider](https://github.com/MSOpenTech/vagrant-azure) on your machine, download your *Publish Settings* and import them, generate the necessary certificates, modify the `Vagrantfile` appropriately, and then run:

```
$ vagrant up
```

You will end up with an Ubuntu 14.04.2 box running on Azure, which you can `ssh` into:

```
$ vagrant ssh
```


## Contributors

* Daniel Perez Alvarez ([unindented@gmail.com](mailto:unindented@gmail.com))


## License

Copyright (c) 2015 Daniel Perez Alvarez ([unindented.org](http://unindented.org/)). This is free software, and may be redistributed under the terms specified in the LICENSE file.
