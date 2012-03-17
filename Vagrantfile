# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "lucid64"

  config.vm.customize do |vm|
    vm.memory_size = 1024
    vm.cpus = 4
  end

  config.vm.network :hostonly, "192.168.51.50"

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "chef/cookbooks"
    chef.add_recipe "apt"
    chef.add_recipe "apache2"
    # chef.json = { :mysql_password => "foo" }
  end
end
