Vagrant.configure(2) do |config|

  config.vm.box = "trusty-cloud-image"

  guest_ip = "dhcp"

  if guest_ip == "dhcp"
    config.vm.network "private_network", type: guest_ip
  else
    config.vm.network "private_network", ip: guest_ip
  end

  config.vm.hostname = "ads-tracking.vm"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "8096"]
  end

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "puppet/manifests"
    puppet.manifest_file = "init.pp"

    puppet.module_path = "puppet/modules"
    puppet.facter = {
      "project_path" => "/home/vagrant/src"
    }
  end

  # project synced folder
  config.vm.synced_folder  ".", "/home/vagrant/src"
end
