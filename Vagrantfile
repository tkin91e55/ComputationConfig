Vagrant.configure(2) do |config|


  #define a new machine: Computer, the termianl machine name
  config.vm.define :Computer do |comp_config|
    comp_config.vm.synced_folder "comp_vagrantSynced", "/vagrant_data", create: true
    comp_config.vm.box = "hashicorp/precise64"
    comp_config.vm.host_name = "computer"
    comp_config.vm.network "private_network", ip: "192.168.35.10"
    comp_config.ssh.insert_key = false

    comp_config.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--name", "computation", "--memory", "512"]
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
  end

  config.vm.host_name = "ubuntu12-64"


end
