# chef_workstation
This is a vagrant file that attempts to create a functioning chef workstation with the following toolset:
* the ChefDK
* Vagrant
* Virtualbox

It is a vagrant box that can create vagrant boxes.

## Requirements
* You must have vagrant and virtualbox installed on your machine.

## Usage
To create the machine
* git clone the repo
* open a shell and cd into the repo
* run vagrant up

To use the machine
* from the repo directory, run vagrant ssh

## Caveats
* Your kitchen/vagrant machines that are created on the using the workstation must be 32 bit machines.  See [this issue](https://github.com/Varying-Vagrant-Vagrants/VVV/issues/375) for more info.
* 
