# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  # Access to Neo4j from the host
  config.vm.network :forwarded_port, guest: 7474, host: 7474
  config.vm.network "forwarded_port", guest: 7687, host: 7687

  # config.vm.network "private_network", ip: "192.168.50.1"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end
