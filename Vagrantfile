# Vagrantfile API/syntax version.
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "hashicorp/precise64"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  #config.vm.network "forwarded_port", guest: 8080, host: 8080

  # If true, then any SSH connections made will enable agent forwarding.
  # Default value: false
  config.ssh.forward_agent = true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/vagrant.yml"
  end
end
