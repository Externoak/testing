Vagrant.configure("2") do |config|
  config.vm.define "Testapache1" do |config|
      config.vm.box = "ubuntu/trusty64"
      config.vm.hostname = "Testapache1"
  config.vm.network "public_network", bridge: "eth1"
     config.vm.provider :virtualbox do |v|
        v.customize ["modifyvm", :id, "--memory", 512]
        v.customize ["modifyvm", :id, "--name", "Testapache1"]
      end
   config.vm.provision :ansible do |ansible|
                      ansible.playbook = "main.yml"
  end
    end
end
