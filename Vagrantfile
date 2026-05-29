Vagrant.configure("2") do |config|

  # Máquina maestra - tierra
  config.vm.define "tierra" do |tierra|
    tierra.vm.box = "debian/bookworm64"
    tierra.vm.hostname = "tierra.sistema.test"
    tierra.vm.network "private_network", ip: "192.168.57.103"
    tierra.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.name = "tierra"
    end
  end

  # Máquina esclava - venus
  config.vm.define "venus" do |venus|
    venus.vm.box = "debian/bookworm64"
    venus.vm.hostname = "venus.sistema.test"
    venus.vm.network "private_network", ip: "192.168.57.102"
    venus.vm.provider "virtualbox" do |vb|
      vb.memory = "512"
      vb.name = "venus"
    end
  end

end