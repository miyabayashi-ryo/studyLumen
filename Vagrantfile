# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.33.14"
  #config.vm.synced_folder "./lumen", "/var/www/lumen"
  
  config.vm.provider "virtualbox" do |vb|
    vb.name = "study_lumen"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "./ansible/playbook.yml"
  end

end
