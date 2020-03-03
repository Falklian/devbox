Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "devbox"
  config.vm.network "public_network", ip: "10.0.0.7", bridge: "br0"
  config.vm.define "devbox"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = 4096
    vb.name = "devbox"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/site.yml"
  end
end
