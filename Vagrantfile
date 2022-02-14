Vagrant.configure("2") do |config|

  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.box = "generic/debian10"
  
  #Master
  config.vm.define "master" do |master|
    master.vm.hostname = "master"
    master.vm.network :private_network, ip: "192.168.60.2"
  end
  
  #Manage host
  config.vm.define "app1" do |app|
    app.vm.hostname = "app1"
    app.vm.network :private_network, ip: "192.168.60.4"
  end

  config.vm.define "app2" do |app|
    app.vm.hostname =  "app2"
    app.vm.network :private_network, ip: "192.168.60.5"
  end

  config.vm.define "db1" do |db|
    db.vm.hostname =  "db1"
    db.vm.network :private_network, ip: "192.168.60.6"
  end
end
