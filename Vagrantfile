# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
  end
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=666"] 
  config.vm.network :forwarded_port, guest: 9000, host: 9000
  config.vm.provision :shell, :path => "install-docker.sh"
  config.vm.provision :shell, :path => "install-docker-compose.sh"
end
