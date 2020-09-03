# Vagrant and Virtual Box 101
This repo setup a simple ubuntu machine.

## What is Vagrant?

Vagrant is software that is used to manage a development environment. Through the command line, you can grab any available OS, install it, configure it, run it, work inside of it, shut it down, and more. Using VirtualBox and Vagrant, you can simulate the production environment of your app or website.

## What is Virtual Box?

Oracle virtualbox is a software which allow users to run multiple operating system in a single machine and to freely switch between OS instances running simultaneously. It can create and manage guest virtual machine each with a guest operating system and its own virtual environment.

## Find out basic Vagrant commands
```
vagrant init
vagrant destroy
vagrant up
vagrant ssh
sudo apt-get update -y
sudo apt-get install nginx -y
sudo systemctl restart nginx
ps aux | grep nginx
exit - exit out of the vm
vagrant reload
```

## Create a ubuntu 18.04 server using vagrant

1) vagrant init <box_distribution>

2) code needed in your VagrantFile

`Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network 'private_network', ip: '192.168.10.100'
end`

3) vagrant up

4) vagrant ssh [PUTS YOU IN THE VIRTUAL BOX]

5) sudo apt-get update -y [UPDATES YOUR LIST OF PACKAGES]

6) sudo apt-get install nginx -y

7) sudo systemctl restart nginx

8) ps aux | grep nginx

9) exit - exit out of the vm

10) copy 192.168.10.100 on the web

## What is -y

gives confirmation before you get a prompt
