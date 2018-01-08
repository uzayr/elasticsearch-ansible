# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/xenial64"
  end
  config.vm.network :private_network, ip: "192.168.33.20"
  config.vm.hostname = "localhost"

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = 'run/run.yml'
      ansible.verbose = "vvv"
  end
end
