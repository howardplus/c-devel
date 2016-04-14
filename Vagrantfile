# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.provider "virtualbox" do |v|
        v.memory = 2048
        v.cpus = 2
    end

    config.vm.box = "ubuntu/trusty64"

    #config.vm.network "forwarded_port", guest: 80, host: 8080
    #
    config.vm.provision :ansible do |ansible|
        ansible.playbook = "playbook.yml"
    end

    config.ssh.forward_agent = true
    config.ssh.forward_x11 = true

end
