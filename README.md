# Vagrant LAMP + GMP!

This project is to help you up and running LAMP fast in local environment.

#Requirement

1. VirtualBox - Download latest from https://www.virtualbox.org/
2. Vagrant - Download latest from https://www.vagrantup.com/

#Running & Installing

1. Clone this repository
2. Cd into this clone repository

For 1st time installation, this might take around 20 minute to download the image and another 10 minute to setup all required webserver package

```
vagrant up
```

Setup webserver using Puppet

```
vagrant provision
```

You should now can access blockstrap framework website through http://192.168.56.101/

To ssh into the webserver:
```
host: 192.168.56.101
user:vagrant
password:vagrant
```

#Shared Apache Web Folder
Apache web directory is in synced folder

#Broken Composer

Suppose puppet will execute composer to install bitwasp but somehow it's broken but git manage to clone it.

To manually install bitwasp:
```
cd /var/www/html/bitwasp
composer require mdanter/ecc
composer install
```