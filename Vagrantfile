#!/Users/jima/.rbenv/shims/ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.define :web do |web|
    web.vm.box = "ubuntu-14.04"
    web.vm.network :private_network, ip: "10.33.33.33"
    web.vm.network :forwarded_port, guest: 80, host: 8011

    web.vm.hostname = "dev.416.bike"

    web.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
    end

    # web.vm.provision :ansible do |ansible|
    #   ansible.playbook = "build-server.yml"
    #   ansible.inventory_path = "hosts-vagrant"
    #   ansible.verbose = "v"
    #   ansible.ask_sudo_pass = true

    #   # https://github.com/mitchellh/vagrant/issues/3096
    #   ansible.limit = 'all'
    # end

  end


end
