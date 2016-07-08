# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/trusty64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://atlas.hashicorp.com/ubuntu/trusty64"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # For information on available options for the Virtualbox provider, please visit:
  # http://docs.vagrantup.com/v2/virtualbox/configuration.html
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  config.vm.define "ansible-test-machine-1"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "base.yml"
    ansible.sudo = true
    ansible.groups = {
      "digitalocean" => ["ansible-test-machine-1"],
      "rpi2" => ["ansible-test-machine-1"],
    }
    # Print out the full command to run ansible
    # ansible.verbose = "v"
  end
end
