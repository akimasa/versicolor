versicolor
=================

My DevOps repos - An idea, afix, etc. you can send me a PullRequest

## Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Homebrew](http://brew.sh/)
* [Git](http://git-scm.com/)
* [Vagrant](http://www.vagrantup.com/)
* [Packer](http://www.packer.io/)

## Quick Start

### OSX

I can start very easily that versicolor to command one run

```
curl https://raw.github.com/ryurock/versicolor/master/setup | ruby -;
vagrant up --provision;

```

or command oneliner

```
curl https://raw.github.com/ryurock/versicolor/master/setup | ruby -; vagrant up --provision;
```

## Usage 

1. Using to Vagrant Login.
```
vagrant ssh
```

1. check Ansible Ping
```
ansible LOCAL -i inventries/local -m ping
```

1. Using Ansible Playbook(test-playbook.yml)
```
ansible-playbook -i ansible/inventories/local ansible/test-playbook.yml 
```

1. Using Ansible Playbook(main)
```
ansible-playbook -i ansible/inventories/local ansible/site.yml 
```

1. Using Serverspec
```
cd serverspec
rake spec
```

## TrableShutting

### An error occurred during installation of VirtualBox Guest Additions x.x.x. Some functionality may not work as intended.

VirtualBox Guest Additions not same VirtualBox version.

```
vagrant vbguest --do rebuild
```

### No installation found.

VirtualBox Guest Additions not install

```
vagrant vbguest --do install
```
