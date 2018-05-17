$script = <<SCRIPT
  sudo yum -y update 
  sudo yum install -y docker
  sudo systemctl enable docker
  sudo systemclt start docker
  sudo yum install -y python-setuptools
  sudo /usr/bin/easy_install pip
  sudo pip install docker-compose
SCRIPT

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"
  config.vm.hostname = "node"
  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.provision "shell", inline: $script
end
