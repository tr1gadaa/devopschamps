# -*- mode: ruby -*-
# vi: set ft=ruby :

 $script = <<-SCRIPT
 sudo apt-get update
 sudo apt-get install -y apache2
 sudo apt install git
 git --version
 SCRIPT

 Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu_jammy64"
  # установим обновления в скрипте
  config.vm.box_check_update = false
     config.vm.hostname = "betterthanyourubuntu"
     config.vm.define "better_than_your_ubuntu"
      config.vm.network "private_network", ip: "192.168.33.10"
      config.vm.synced_folder "../data", "/vagrant_data"
      config.vm.provision "shell", inline: $script

 end