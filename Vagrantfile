# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network :public_network

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
  end

  config.vm.synced_folder "/home/user/Projects/", "/home/vagrant/projects"

  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :private_network, ip: "79.132.125.153"
end
