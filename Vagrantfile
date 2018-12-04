# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 1234
  config.vm.define :easyengine4
  config.vm.provider :virtualbox
  config.vm.provision "shell", inline: <<-SHELL
    wget -qO ee rt.cx/ee4 && sudo bash ee
    ee site create localhost
  SHELL
end
