# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "master-vm" do |vm1|
    vm1.vm.hostname = "master-vm"
    vm1.vm.box = "2204"
    vm1.vm.network "private_network", ip: "192.168.122.11"

    vm1.vm.provider "libvirt" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
    vm1.vm.provision "shell", run: "always", inline: <<-SHELL
      echo "Hello From The Master VM"
    SHELL
  end
  config.vm.define "worker-one" do |wk1|
    wk1.vm.hostname = "worker-one"
    wk1.vm.box = "2204"
    wk1.vm.network "private_network", ip: "192.168.122.12"

    wk1.vm.provider "libvirt" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
    wk1.vm.provision "shell", run: "always", inline: <<-SHELL
      echo "Hello From The Worker ONE"
    SHELL
  end
  config.vm.define "worker-two" do |wk2|
    wk2.vm.hostname = "worker-two"
    wk2.vm.box = "2204"
    wk2.vm.network "private_network", ip: "192.168.122.13"

    wk2.vm.provider "libvirt" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
    wk2.vm.provision "shell", run: "always", inline: <<-SHELL
      echo "Hello From The Worker TWO"
    SHELL
  end
end
