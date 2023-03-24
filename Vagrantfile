Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64" # choose the Ubuntu version you prefer
  config.vm.network "forwarded_port", guest: 8080, host: 8080 # forward port 8080
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096" # set the amount of RAM you want to allocate to the VM
    vb.cpus = "2" # set the number of CPUs you want to allocate to the VM
  end
 config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get -y install git build-essential libssl-dev libffi-dev python3-dev python3-pip
    sudo pip3 install --upgrade setuptools
    wget -q https://github.com/ekristen/cast/releases/download/v0.14.0/cast_v0.14.0_linux_amd64.deb
    sudo dpkg -i cast_v0.14.0_linux_amd64.deb
	cp ./cast /usr/local/bin/cast
    sudo cast install teamdfir/sift-saltstack
    echo "export PATH=$PATH:/usr/local/bin" >> ~/.bashrc
    source ~/.bashrc
  SHELL

end
