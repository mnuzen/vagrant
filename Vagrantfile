# _*_ mode: ruby _*_

VAGRANT_API_VERSION = "2"

Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network :forwarded_port, guest: 8080, host: 80, auto_correct: true
  
  # this specifies the ip address 
  #config.vm.network :private_network, ip: "192.168.68.8"
  dir = File.expand_path("..", __FILE__)
  puts "DIR: #{dir}"

  config.vm.provision "shell", path: File.join(dir, ".provision/bootstrap.sh")
end
