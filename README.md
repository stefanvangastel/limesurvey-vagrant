LimeSurvey Vagrant development box
=======================

## Overview

Vagrant is a great tool to automate creating and configuring lightweight, reproducible, and portable development environments. If you are new to Vagrant you might want to take a look at [official documentation](http://docs.vagrantup.com/v2/why-vagrant/index.html) to get a basic gist who is it for and why to use it.

This Vagrantfile creates a simple Ubuntu 14.04 x64 server box with PHP, MySQL and Apache2. The latest LimeSurvey sourcecode is cloned into the VM and shared with the directory you run `vagrant up` from so you can start developing right away.

## Host OS software prerequisites:

- Vagrant depends on Oracle's [VirtualBox](https://www.virtualbox.org/) to create all of its virtual environments.
- Download and install [Vagrant](http://vagrantup.com)

## Installation:

- Make sure you've installed prerequisites
- Open terminal,`cd` to working directory and clone the project:
- `git clone https://github.com/stefanvangastel/limesurvey-vagrant.git`
- Run `vagrant up` to start and provision the machine
- Run web browser and go to `http://192.168.33.98/`

- To log into the vagrant box execute `vagrant ssh`
- To turn off virtual machine execute `vagrant halt`
- To start the virtual machine again run `vagrant up` again
- To clean up and remove all traces of the virtual machine execute `vagrant destroy`

## Default connection parameters

    Virtual machine IP:     192.168.33.98
    System user:            vagrant
    System password:        vagrant
    MySQL user:             root
    MySQL password:         lsdev

## Packages and libraries that come with the box

- apache2
- php5 (5.5)
- php5-cli
- php5-mysql
- php5-dev
- mysql-server
- git-core
- vim
- curl
