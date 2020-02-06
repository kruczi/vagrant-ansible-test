# -*- mode: ruby -*-
# vi: set ft=ruby :
 
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
 
  config.vm.define "drupal" do |drupal|
    drupal.vm.box = "geerlingguy/ubuntu1804"
    drupal.vm.hostname = "drupal"
    drupal.vm.network "private_network", ip: "192.168.33.10"
    drupal.vm.network "forwarded_port", guest: 80, host: 8080
  end

    # VirtualBox.
  config.vm.provider :virtualbox do |v|
    v.linked_clone = true
    v.customize ['modifyvm', :id, '--natdnshostresolver1', 'on']
    v.customize ['modifyvm', :id, '--ioapic', 'on']
    v.customize ['modifyvm', :id, '--audio', 'none']
  end
 
end