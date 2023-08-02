# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Base VM OS configuration.
  config.vm.box = "geerlingguy/centos7"
  config.vm.network :private_network, ip: "192.168.56.66"
  config.ssh.insert_key = false
  config.vm.synced_folder '.', '/vagrant', disabled: true

  config.vm.hostname = "docker-middleware.test"
  config.vm.provider :virtualbox do |v|
    v.name = "docker-flmiddlewareask.test"
    v.memory = 8192
    v.cpus = 4
  end

  # Enable provisioning with Ansible.
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/main.yml"
  end
end
