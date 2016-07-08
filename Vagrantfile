# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/centos-7.2"
  config.vm.hostname = "vagrant-foreman.localdomain"

  # static host-only adapter, other servers will find foreman here
  config.vm.network "private_network", ip: '10.127.127.127'

  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
  end

  # forward admin port
  config.vm.network "forwarded_port", guest: 443, host: 8443

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant/playbook.yml"
  end
end
