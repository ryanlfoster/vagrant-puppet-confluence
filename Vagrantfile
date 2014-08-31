# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "confluence1" do |confluence1|
    confluence1.vm.box      = "centos65"
    confluence1.vm.hostname = "confluence.home"
    confluence1.vm.network :private_network, ip: "192.168.33.10"
    confluence1.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-64-x64-vbox4210.box"
  end
  config.vm.define "confluence2" do |confluence2|
    confluence2.vm.box      = "centos59"
    confluence2.vm.hostname = "confluence.home"
    confluence2.vm.network :private_network, ip: "192.168.33.11"
    confluence2.vm.box_url  = "http://puppet-vagrant-boxes.puppetlabs.com/centos-59-x64-vbox4210.box"
  end
  config.vm.define "confluence3" do |confluence3|
    confluence3.vm.box      = "ubuntu1204"
    confluence3.vm.hostname = "confluence.home"
    confluence3.vm.network :private_network, ip: "192.168.33.12"
    confluence3.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/ubuntu-server-12042-x64-vbox4210.box"
  end

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.module_path    = "modules"
    puppet.manifest_file  = "site.pp"
    puppet.options = "--verbose"
  end

end
