# Vagrant
---
Vagrant allows for Virtual Machines to be quickly setup, and easy to use.
## Download Vagrant
---
To download vagrant [https://www.vagrantup.com/downloads.html]("https://www.vagrantup.com/downloads.html")

## Create Vagrant File
---
To create vagrant file
```bash
vagrant init
```

Or you can with box
```bash
vagrant init ubuntu/groovy64
```
## Prepare Vagrant File
---
### Vagrant Box

View list of vagrant's box [https://app.vagrantup.com/boxes/search]("https://app.vagrantup.com/boxes/search")

Add box into your vagrant file
```
config.vm.box = "ubuntu/groovy64"
```

### Network
```
config.vm.network "private_network", ip: "192.168.33.10"
```

### Shared Folder
```
config.vm.synced_folder "D:/your_project_location", "/var/www/html"
```
### Virtual Machine
Using *Virtualbox*
```
config.vm.provider "virtualbox" do |vb|
    vb.name = "TestMachine"             # Machine name
    vb.cpus = 2                         # CPU
    vb.memory = 4096                    # Memory
end
```
### Start Your Machine
To create and start your machine
Open terminal or git bash or powershell from your vagrant file location
```bash
vagrant up
```

If you use multiple VM, you should provide the name
```bash
vagrant up name
```
### SSH
To control your machine
```bash
vagrant ssh
```
If you use multiple VM, you should provide the name
```bash
vagrant ssh name
```

## Setup Ubuntu
---
### Update Ubuntu
After you get into ubuntu
First important, you need to update ubuntu
```bash
sudo apt update && sudo apt upgrade -y
```

### Install Apache2
```bash
sudo apt install apache2 -y
```

### Install PHP7.4
```bash
sudo apt -y install software-properties-common
```
```bash
sudo add-apt-repository ppa:ondrej/php
```
```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt -y install php7.4
```

### Install PHP7.4 extension
```bash
sudo apt -y install php7.4-curl
```
```bash
sudo apt -y install php7.4-fpm
```
```bash
sudo apt -y install php7.4-gd
```
```bash
sudo apt -y install php7.4-bcmath
```
```bash
sudo apt -y install php7.4-mbstring
```
```bash
sudo apt -y install php7.4-xml
```
Database driver for mysql
If you use other database you should install other
```bash
sudo apt -y install php7.4-mysql
```
```bash
sudo apt -y install php7.4-zip
```
Restart Apache2 service
```bash
sudo systemctl restart apache2
```
### Install Composer
```bash
sudo apt -y install zip
```
```bash
cd ~
curl -sS https://getcomposer.org/installer -o composer-setup.php
```
```bash
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```
### Install MySQL
```bash
sudo apt install mysql-server -y
```

---