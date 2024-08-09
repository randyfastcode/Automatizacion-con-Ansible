Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  (1..3).each do |i|
    config.vm.define "server#{i}" do |server|
      server.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
        vb.cpus = 1
      end
      server.vm.hostname = "server#{i}"
    end
  end
end
