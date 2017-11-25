# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

VAGRANT_VERSION = "2"
Vagrant.configure(VAGRANT_VERSION) do |config|
  
  config.vm.box = "hashicorp/precise64"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "ansible" do |ansible|
  	ansible.playbook = "ansible/playbook.yml"
  	ansible.inventory_path = "ansible/hosts"
  	ansible.limit = "VM1"
  	ansible.sudo = true
  end
  
end
