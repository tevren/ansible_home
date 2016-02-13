Vagrant.configure(2) do |config|
  config.vm.box = "debian/jessie64"
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider :virtualbox do |vb|
    vb.name = "storage.dev"
    vb.memory = 1024
    vb.cpus = 1
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "storage.yml"
    ansible.verbose = "v"
  end
end
