# Vagrant Multi Machine
Vagrant Multi Machine is a template for multiple VM's running on Ubuntu.

## Requirements
VirtualBox 6.1
Vagrant 2.2.13

## Setup
Clone project and run:

`vagrant up`

After the command is finished run:

`vagrant ssh server1`

Check hostname:

`hostname -I`

SSH to the other VM by running the command:

`ssh vagrant@192.168.50.12`

Enter `yes` and enter password:

`vagrant`

Check hostname again.


