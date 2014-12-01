# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# Require a recent version of vagrant otherwise some have reported errors setting host names on boxes
Vagrant.require_version ">= 1.6.2"

Vagrant.configure("2") do |config|

    config.vm.provider :virtualbox do |v|
        v.name = "LimeSurvey"
        v.customize ["modifyvm", :id, "--memory", 512]
    end

    config.vm.box = "ubuntu/trusty64"

    config.vm.network :private_network, ip: "192.168.33.98"
    config.ssh.forward_agent = true

  	config.vm.synced_folder "./", "/vagrant", id: "vagrant-root",
	    owner: "vagrant",
	    group: "www-data",
	    mount_options: ["dmode=775,fmode=664"]

    config.vm.provision :shell, path: "provision.sh"
end

