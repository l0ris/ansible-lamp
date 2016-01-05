# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.
  

  config.vm.box = "puppetlabs/centos-6.6-64-nocm"
  config.vm.hostname = "centos-lamp"
  

  # network config
  config.vm.network :private_network, ip: "192.168.56.101"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  

  # Run our ansible modules
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.sudo = true
  end

end
