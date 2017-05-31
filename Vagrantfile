Vagrant.configure("2") do |config|
  config.vm.define "Testapache1" do |config|
      config.vm.boot_timeout = 1200
      config.vm.box = "ubuntu/trusty32"
      config.vm.hostname = "Testapache1"
  config.vm.network "public_network", bridge: "eth1"
   config.vm.provision :ansible do |ansible|
                      ansible.playbook = "main.yml"
  end
    end
end
