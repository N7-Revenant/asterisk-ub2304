# -*- mode: ruby -*-
# vi: set ft=ruby :

PROJECT_NAME = "Predictive 23.04 ENV"
BOX_REPO_URI = 'https://tc-build.telecontact.ru/artifact/repository/Vagrant.telecc/base-boxes'

Vagrant.configure("2") do |config|
  config.vm.box_url = "#{BOX_REPO_URI}/ubuntu-2304-amd64/lunar-server-cloudimg-amd64-vagrant.box"
  config.vm.box = "ubuntu-2304-amd64"

  config.vm.provider 'virtualbox' do |machine|
    machine.name = "ub2304"
    machine.memory = 512
    machine.cpus = 1
  end

  config.vm.define "ub2304" do |host|
    host.vm.hostname = "ub2304"
    host.vm.network "private_network", ip: "192.168.56.71"
  end

  config.vm.provision "shell", path: "bootstrap.sh"
end
