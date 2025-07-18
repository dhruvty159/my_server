Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  # Forward a port (e.g., for SSH or web server access)
  config.vm.network "forwarded_port", guest: 81, host: 8081

  # Set up private network (optional)
  config.vm.network "private_network", type: "dhcp"

  # Provision with a shell script (optional)
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y nginx
  SHELL
end

