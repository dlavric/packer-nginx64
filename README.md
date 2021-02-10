## Packer Base for learning

### Repository is using Packer to create a Vagrant virtual box with Ubuntu LTS and Nginx

### Prerequisites
- [X] [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

- [X] [Vagrant](https://www.vagrantup.com/downloads)

- [X] [Packer](https://www.packer.io/downloads)

## How to Use the Repo
- Clone this repo:
```shell
$ git clone git@github.com:dlavric/packer-nginx64.git
```

- Go to the directory where the repo is stored
```shell
$ cd packer-nginx64
```

- Start Packer
```shell
$ packer build template.json
```

- Add the box to Vagrant 
```shell
vagrant box add --name nginx64 nginx64-vbox.box
```

- Initialize Vagrant with the local box created with Packer
```shell
$ vagrant init nginx64-vbox.box
```

- Start Vagrant
```shell
$ vagrant up
```

- Access the Vagrant machine
```shell
$ vagrant ssh
```

- Logout from Vagrant
```shell
$ logout
```

- Destroy Vagrant
```shell
$ vagrant destroy
```