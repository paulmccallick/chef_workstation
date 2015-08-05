# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
  end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get update
     sudo apt-get install -y virtualbox-source module-assistant
     sudo apt-get install -y linux-headers-3.2.0-23 linux-headers-3.2.0-23-generic
     sudo m-a -t -f -q prepare
     sudo m-a -t -q a-i virtualbox-source
     sudo apt-get install -y virtualbox
     wget --progress=dot https://dl.bintray.com/mitchellh/vagrant/vagrant_1.7.4_x86_64.deb
     wget --progress=dot https://opscode-omnibus-packages.s3.amazonaws.com/ubuntu/12.04/x86_64/chefdk_0.6.2-1_amd64.deb
     sudo dpkg -i chefdk_0.6.2-1_amd64.deb
     sudo dpkg -i vagrant_1.7.4_x86_64.deb
  SHELL
end
