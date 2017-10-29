Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.name = "locust"
  config.vm.hostname = "locust"
  config.vm.network "forwarded_port", guest: 8089, host: 8089
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "locust.yml"
  end
end
