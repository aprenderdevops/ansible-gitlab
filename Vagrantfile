Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
    config.vm.boot_timeout = 120
    config.vm.hostname = "gitlab"
    
    config.vm.provider "virtualbox" do |vb|
        vb.memory = 2048
        vb.cpus = 2
        vb.name = "gitlab"
    end
    
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "provision/install.yml"
        ansible.host_key_checking = false
        ansible.sudo = true
        ansible.tags = ['gitlab']
    end
    
    config.vm.network "private_network", ip: "192.168.107.20"
    config.vm.network "forwarded_port", host: 8080, guest: 80, autocorrect: true
end