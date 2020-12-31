# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # Box
    config.vm.box = "ubuntu/groovy64"

    # IP Address
    config.vm.network "private_network", ip: "192.168.33.10"

    # Shared Folder
    config.vm.synced_folder "D:/your_project_location", "/var/www/html"

    # Virtual Machine
    config.vm.provider "virtualbox" do |vb|
        vb.name = "Softbank"
        vb.cpus = 2
        vb.memory = 4096
    end
end