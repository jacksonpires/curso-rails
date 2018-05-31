# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox"
  config.vm.box = "jacksonpires/curso-rails"
  config.vm.box_version = "1.0.0"
 
  config.vm.network :forwarded_port, guest: 3000, host: 3000 # rails
  config.vm.network :forwarded_port, guest: 8181, host: 8181 # cloud9

  config.vm.provider "virtualbox" do |vb|
    vb.customize [ "modifyvm", :id, "--uartmode1", "disconnected" ]
  end

  config.vm.provision "shell", privileged: false, run: "always", inline: $START_CLOUD9_IDE
end

$START_CLOUD9_IDE = <<SCRIPT
  echo "Start Cloud9 IDE Standalone application"
  /home/vagrant/.nvm/versions/node/v10.1.0/bin/forever start /home/vagrant/Cloud9IDE/server.js -p 8181 -l 0.0.0.0 -a : -w "/vagrant/workspace"
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "."
  echo "Now you can access Cloud9 on http://localhost:8181"
SCRIPT
