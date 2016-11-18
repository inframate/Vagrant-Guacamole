# -*- mode: ruby -*-
 
# vi: set ft=ruby :
 
hosts = {
 

  
    "GuacamoleVM" => "192.168.88.100",


 
}
 
Vagrant.configure("2") do |config|
 
    config.vm.box = "bento/centos-7.1"
#   config.ssh.insert_key = false
#   config.ssh.private_key_path = ["id_rsa",  "~/.vagrant.d/insecure_private_key"]
#	config.vm.provision "file", source: "id_rsa.pub", destination: "~/.ssh/authorized_keys"
	config.vm.provision :shell, path: "Provision-script.sh" 
	
		hosts.each do |name, ip|
 
		config.vm.define name do |machine|
	 
			machine.vm.network :private_network, ip: ip
	 
			machine.vm.provider "virtualbox" do |v|
	 
				v.name = name
				v.customize [
					"modifyvm", :id,
					"--memory", "1024",
					"--cpus", "1"
				]
			end
			machine.vm.hostname = name
		end
     
	end
    
end


