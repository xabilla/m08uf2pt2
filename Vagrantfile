Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian11"
  config.vm.hostname = "dacomo"
  config.vm.provider "virtualbox" do |v|
    # v.gui = true
    v.name = "m08uf1pr3"
    v.memory = 2048
    v.cpus = 2
    v.customize ['modifyvm', :id, '--clipboard', 'bidirectional']     
  end
  
  # config.vm.network "forwarded_port", guest: 80, host: 10080 
  # config.vm.network "forwarded_port", guest: 10081, host: 10081
  
  config.vm.network "public_network" 
    
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update -y
    # sudo apt-get upgrade -y
    sudo apt-get install -y net-tools
    sudo apt-get install -y aptitude
  SHELL

end
