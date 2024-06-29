# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.define "master" do |machine_01|
    machine_01.vm.box = "ubuntu/bionic64"
    machine_01.vm.network "private_network", ip: "192.168.57.201"
    machine_01.vm.hostname = "master"
    machine_01.vm.provider "virtualbox" do |vb|
      vb.name = "master"
      vb.memory = 400
      vb.cpus = 1
    end
  end
  config.vm.define "node_01" do |machine_02|
    machine_02.vm.box = "ubuntu/bionic64"
    machine_02.vm.network "private_network", ip: "192.168.57.202"
    machine_02.vm.hostname = "node01"
    machine_02.vm.provider "virtualbox" do |vb|
      vb.name = "node_01"
      vb.memory = 400
      vb.cpus = 1
    end
  end


end
