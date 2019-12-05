

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "centos"
  config.vm.network :private_network, ip: "192.168.200.6"
  config.vm.boot_timeout = 600

  config.vm.provider :virtualbox do |vb|
    vb.customize [
      "modifyvm", :id,
      "--memory", "2048",  "--cpus", "1"
    ]
  end
end
