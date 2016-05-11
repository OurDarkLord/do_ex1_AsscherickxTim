Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "tim.be"
  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.network :private_network, ip: "192.168.33.10"
  config.vm.provision "shell", inline: "apt-get update"
  config.vm.provision "shell", inline: "apt-get upgrade -y"
  config.vm.provision "shell", inline: "apt-get install nginx"
  config.vm.provision "shell", inline: "rm /etc/nginx/sites-enabled/default"
  config.vm.provision "shell", inline: "ln -s /vagrant/do_ex1_site/default /etc/nginx/sites-enabled/default"
  config.vm.provision "shell", inline: "service nginx restart"
end