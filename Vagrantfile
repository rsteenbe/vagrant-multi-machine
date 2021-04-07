Vagrant.configure("2") do |config|
  config.vm.define "server1" do |server1|
    server1.vm.box = "bento/ubuntu-20.04"
	server1.vm.network 'forwarded_port', guest: 8180, host: 8180
	server1.vm.network "private_network", ip: "192.168.50.10"
	server1.vm.provider "virtualbox" do |v|
		v.memory = 4096
		v.cpus = 2
	end
	server1.vm.provision "shell", inline: <<-SHELL
    /bin/echo "================= Client Server Running ================"
	SHELL
	config.ssh.username = "vagrant"
	config.ssh.password = "vagrant"
  end
  
  config.vm.define "server2" do |server2|
    server2.vm.box = "bento/ubuntu-20.04"
	server2.vm.network 'forwarded_port', guest: 8181, host: 8181
	server2.vm.network "private_network", ip: "192.168.50.12"
	server2.vm.provider "virtualbox" do |v|
		v.memory = 4096
		v.cpus = 2
	end
	server2.vm.provision "shell", inline: <<-SHELL
    /bin/echo "================= Client Server Running ================"
	SHELL
	config.ssh.username = "vagrant"
	config.ssh.password = "vagrant"
  end
end