# -*- mode: ruby -*-
# vi: set ft=ruby :

# One machine only
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 80, host: 80, host_ip: "127.0.0.1"
  config.vm.network "forwarded_port", guest: 8080, host: 10051, host_ip: "127.0.0.1"
  config.vm.network "private_network", ip: "192.168.33.10",  auto_config: true
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
  end
  # Ansible call
end
