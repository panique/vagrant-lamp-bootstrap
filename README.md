# vagrant-lamp-bootstrap

A super-simple Vagrantfile / bootstrap.sh to setup a LAMP stack inside Vagrant 100% automatically.

### Whaaaaat ?

This is a reduced-to-the-max Vagrant setup file for a quick development stack. It will:

* setup a Ubuntu 14.04 LTS "Trustry Thar" 64bit box

* make the box accessable by the host at IP `192.168.33.22`

* sync the current folder with `/var/www/html` inside the box

* automatically perform all the commands in bootstrap.sh directly after setting up the box for the first time

The bootstrap.sh will:

* update, upgrade

* create a folder inside /var/www/html

* install apache 2.4, php 5.5, MySQL, PHPMyAdmin, git and Composer

* also setting a pre-chosen password for MySQL and PHPMyAdmin

* activate mod_rewrite and add *AllowOverride All* to the vhost settings

You can folder and password inside the bootstrap.sh for sure.

### How to use ?

Put `Vagrantfile` and `bootstrap.sh` inside a folder and do a `vagrant up` on the command line.
This box uses Ubuntu 14.04 LTS "Trustry Thar" 64bit, so if you don't have the basic box already, do a 
`vagrant box add ubuntu/trusty64` before.

### Why ?

This is just my personal time-saving bootstrap for Vagrant, it might be useful for you too.
