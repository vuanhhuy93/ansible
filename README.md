# ansible-docker

Installation docker for Ubuntu 22.04 LTS.

## Prerequisites

In order to install docker, you have to launch this script with ansible (the automation tool) on your machine.

Ansible is avaiblable on linux with the following installation example on Ubuntu : 
```
sudo apt update
sudo apt install software-properties-common
sudo apt install ansible
```

You need to have a ssh connection in the target machine (and set the user that will be used in the customizing section).

## Customizing 

First, you have to copy these files :
vars/parameters.yml.example --> vars/parameters.yml
hosts.example --> hosts


You have to customizing some values in these before launching the ansible tool.

You need to set the hosts where you want to install docker. To do this, you just need to add/remove your hosts in the host file of the project.

Then, you have to set the user that will be used for the ssh connection. You have to set it in the vars/parameters.yml file.



## Launch the playbook

You have to execute the script with the following command (assuming you are in the project location) : 

```
ansible-playbook -i hosts/dev playbook.yml 
```


