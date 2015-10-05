# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define :dev do |dev_config|
    dev_config.vm.box = "ubuntu/trusty64"
    dev_config.vm.hostname = "dev"
    dev_config.vm.network "private_network", ip: "192.168.33.10"
    dev_config.vm.provider "virtualbox" do |vb|
        vb.memory = "512"
      end
    dev_config.vm.provision "shell", path: "bootstrap-mgmt.sh"
  end

  config.vm.define :prod do |prod_config|
    prod_config.vm.box = "ubuntu/trusty64"
    prod_config.vm.hostname = "prod"
    prod_config.vm.network "private_network", ip: "192.168.33.11"
    prod_config.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
    end
  end
  
end
