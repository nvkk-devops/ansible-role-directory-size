# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.require_version ">= 1.7.0"

Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-18.04" 

  config.ssh.insert_key = false  
  config.vm.network "forwarded_port", guest: 80, host: 8080
  
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "7168"
    vb.cpus = 1
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end
  
end
