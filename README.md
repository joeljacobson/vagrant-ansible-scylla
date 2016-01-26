##Introduction

Easily provision 3 ScyllaDB nodes across 3 VMs using Ansible with Vagrant & Virtualbox.

##Prerequisites

* [Virtualbox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](http://docs.ansible.com/intro_installation.html)

##Provisioning

Clone the project: ```git clone https://github.com/joeljacobson/vagrant-ansible-scylla.git```

In the project directory enter: ```vagrant up```

Your cluster will be ready shortly depending on your internet connection. The initial boot takes some time as Ansible has to download, install and configure Scylla across each VM. Subsequent reboots are fast.

Scylla will be automatically configured and started once installed. Its will also be automatically started each time the VMs are booted.

Nodes will be running on: ```192.168.56.11```, ```192.168.56.12```, ```192.168.56.13```

SSH into a node with: ```vagrant ssh <nodename>```

Shutdown the VMs: ```vagrant halt```

Resume VMs: ```vagrant up```

Destroy the VMs (requires re-provisioning): ```vagrant destroy```

