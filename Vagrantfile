Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"
  config.vm.disk :disk, size: "50GB", primary: true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "local-machine.yml"
  end

  config.vm.provider :libvirt do |libvirt|
      libvirt.cpus = 2
      libvirt.memory = 4096
  end
end
