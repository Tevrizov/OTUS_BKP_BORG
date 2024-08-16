Vagrant.configure(2) do |config|
    config.vm.box = "ubuntu/jammy64"

    config.vm.provision "ansible" do |ansible|
          #  ansible.verbose = "vvv"
            ansible.playbook = "playbook.yml"
         #   ansible.inventory_path = "ansible_hosts"
            ansible.become = "true"
          end
        
        
         config.vm.provider "virtualbox" do |v|
           v.memory = 1024
           v.cpus = 1
         end


    config.vm.define "server" do |server|
      server.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: "net1"
      server.vm.hostname = "server"
    end


    config.vm.define "client" do |client|
      client.vm.network "private_network", ip: "192.168.50.11", virtualbox__intnet: "net1"
      client.vm.hostname = "client"
    end


   end


