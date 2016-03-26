VAGRANTFILE_API_VERSION = "2"

vmname="ubuntu-vagrant"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "ubuntu"
    config.vm.box_url = "http://127.0.0.1/ifce.box"
 
    ## Guest Config
    config.vm.hostname = vmname
    config.vm.network :private_network, ip: "192.168.56.12"
    config.vm.network :forwarded_port, guest:8000, host:8000 # forwarding of port 

    ## CPU & RAM
    config.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--cpuexecutioncap", "100"]
        vb.memory = 2048
        vb.cpus = 1
        vb.name = vmname
    end

    ## SSH config
    #config.ssh.private_key_path = "~/.ssh/id_rsa"
    #config.ssh.forward_agent = true
    #config.ssh.insert_key = false

    # Shared fold
    config.vm.synced_folder "./projeto", "/home/vagrant/projeto", create: true

    #config.vm.provision "shell", inline: <<-SHELL
    #    sudo apt-get update
    #SHELL
    config.vm.provision :shell, privileged: false, :path => "setup/install.sh"

end
