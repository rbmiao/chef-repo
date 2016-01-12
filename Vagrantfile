Vagrant.configure("2") do |config|
  config.vm.box = "opscode-ubuntu-14.10"
  config.vm.box_url="https://opscode-vm-bento.s3.amazonaws.com/vagrant/parallels/opscode_ubuntu-14.10-i386_chef-provisionerless.box"
  config.omnibus.chef_version = :latest
  
  config.vm.provision :chef_client do |chef|
  	chef.provisioning_path = "/etc/chef"
  	chef.chef_server_url = "https://api.chef.io/organizations/rbmiao"
  	chef.validation_key_path = "rbmiao-validator"
  	chef.node_name = "miaoserver"
  end
end	