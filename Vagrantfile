VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Ubuntu Server 14.04.5 LTS Trusty Tahr (64-bit): https://vagrantcloud.com/box-cutter/boxes/ubuntu1404-desktop
  config.vm.box = "box-cutter/ubuntu1604-desktop"

  # forward ssh agent and X11
  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true

  # Create a forwarded port
  config.vm.network "forwarded_port", guest: 8181, host: 8181
  
  # configure virtualbox provider
  config.vm.provider "virtualbox" do |v|
    v.name = "FASTMaple"
    v.gui = true
    v.memory = "2048"
  end

  # run ./bootstrap.sh
  config.vm.provision :shell, :path => "bootstrap.sh"

end
