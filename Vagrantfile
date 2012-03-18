# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "lucid64"

  config.vm.customize do |vm|
    vm.memory_size = 2048
    vm.cpus = 8
  end

  config.vm.network :hostonly, "192.168.51.50"

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = ["chef/cookbooks", "chef/custom_cookbooks"]
    chef.add_recipe "example_app"
  end
end
