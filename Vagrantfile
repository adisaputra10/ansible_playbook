Vagrant.configure("2") do |config|
#  config.vm.provision "shell", inline: "apt-get update && apt-get install -y  docker.io "
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/xenial64"
	  master.vm.boot_timeout = 600
    master.vm.network "private_network",ip: "192.168.101.2"
  end
  config.vm.provider :virtualbox do |v|
   v.customize ["modifyvm", :id, "--memory", 2048]
  end
end