Vagrant.configure("2") do |config|
  # Box
  config.vm.box = "ubuntu/bionic64"
  
  # Provider
  config.vm.provider "virtualbox" do |vb|
    vb.name = "NGINX server"
    vb.memory = 512
    vb.cpus = 1
  end

  # Network
  config.vm.network "private_network", ip: "192.168.33.10"

  # Provisioning
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y nginx
  SHELL
 
  # Syncing folder
  config.vm.synced_folder "html", "/var/www/html"
end