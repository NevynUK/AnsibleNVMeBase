# Adding NVMe Drive to Raspberry Pi

This repository contains the scripts necessary to add and NVMe drive to a Raspberry Pi using Ansible.

These scripts are part of a series about automating the setup and configuration of a Raspberry Pi for use in a testing environment.

A full discussion of these scripts can be found in the repeatable deployment series of posts:

* [Part 1 - Initials Setup](https://blog.mark-stevens.co.uk/2024/03/repeatable-deployments-part-1/)
* [Part 2 - NVMe Base](https://blog.mark-stevens.co.uk/2024/03/repeatable-deployments-part-1/)
* [Part 3 - Adding NVMe Drive Automatically](https://blog.mark-stevens.co.uk/2024/07/repeatable-deployments-3-adding-nvme-drive-automatically/)
* [Part 4 - Variables and Samba](https://blog.mark-stevens.co.uk/2024/10/repeatable-deployments-4-variables-and-samba/)

## Assumptions

By default the system assumes the following:

* The Raspberry Pi name will be _testserver500_ and is accessible on the local next work as _testserver500.local_
* The Raspberry Pi already has an operating system installed
* User name is _clusteruser_
* Password for the user is stored in the environment variable _CLUSTER_PASSWORD_

## Ansible Variables

A number of configuration variables have been used to control the behaviour of these scripts.  A description of these variables can be found in the [group_vars/readme](Scripts/group_vars/readme.md) file.

## Instructions

* Edit the hosts.ini_ file if you wish to change any of the default names.
* Updated the operating system with the command _ansible-playbook UpdateAndRebootRaspberryPi.yml_
* Install the NVMe drive with the command _ansible-playbook ConfigureNVMeBase.yml_
* Install Samba with the command _ansible-playbook InstallSamba.yml_

