Vagrant.configure('2') do |config|
  config.vm.box      = 'precise64'
  config.vm.hostname = 'oracle-dev-box'
  config.vm.network :forwarded_port, guest: 1521, host: 1521

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = 'puppet/manifests'
    puppet.module_path    = 'puppet/modules'
  end

  # Provider-specific configuration so you can fine-tune various backing
  # providers for Vagrant. These expose provider-specific options.
  config.vm.provider :virtualbox do |vb|
    # Use VBoxManage to customize the VM
    vb.customize ["modifyvm", :id,
                  "--name", "oracle",
                  # Oracle claims to need 512MB of memory available minimum
                  "--memory", "512",
                  # Enable DNS behind NAT
                  "--natdnshostresolver1", "on"]
  end
end
