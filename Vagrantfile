# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.

  #config.vm.define "s1" do |s1|
  #  s1.vm.box = "CumulusCommunity/cumulus-vx"
  #end

  #config.vm.define "s2" do |s2|
  #  s2.vm.box = "CumulusCommunity/cumulus-vx"
  #end

  config.vm.define "r1" do |r1|
    m0.vm.box = "CumulusCommunity/cumulus-vx"
    m0.vm.network "private_network", virtualbox__intnet: "link1", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link2", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link4", auto_config: false
  end

  config.vm.define "r2" do |r2|
    m0.vm.box = "CumulusCommunity/cumulus-vx"
    m0.vm.network "private_network", virtualbox__intnet: "link2", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link3", auto_config: false
  end

  config.vm.define "r3" do |r3|
    m0.vm.box = "CumulusCommunity/cumulus-vx"
    m0.vm.network "private_network", virtualbox__intnet: "link4", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link5", auto_config: false
  end

  config.vm.define "r4" do |r4|
    m0.vm.box = "CumulusCommunity/cumulus-vx"
    m0.vm.network "private_network", virtualbox__intnet: "link3", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link5", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link6", auto_config: false
  end

  config.vm.define "sw1" do |sw1|
    m0.vm.box = "CumulusCommunity/cumulus-vx"
    m0.vm.network "private_network", virtualbox__intnet: "link7", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link8", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link9", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link10", auto_config: false
    m0.vm.network "private_network", virtualbox__intnet: "link11", auto_config: false
  end

  config.vm.define "a1" do |a1|
    a1.vm.box = "ubuntu/bionic64"
    #a1.vm.synced_folder "automation/", "/automation"
    #a1.vm.network "forwarded_port", guest: 80, host: 8080
    #a1.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "provisioning/a.yml"
    #end
    a1.vm.network "private_network", virtualbox__intnet: "m0a1", auto_config: false
  end

  #config.vm.define "rtr" do |rtr|
  #  rtr.vm.box = "ubuntu/bionic64"
  #  rtr.vm.network "private_network", virtualbox__intnet: "public", auto_config: false
  #  rtr.vm.network "private_network", virtualbox__intnet: "m0rtr", auto_config: false
  #end

  #config.vm.define "h1" do |h1|
  #  h1.vm.box = "ubuntu/trusty64"
  #end

  #config.vm.define "h2" do |h2|
  #  h2.vm.box = "ubuntu/trusty64"
  #end

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
