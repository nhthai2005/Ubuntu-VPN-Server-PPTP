Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.network "private_network", ip: "172.16.10.210"
    config.vm.hostname = "vpn-server"
    #  config.vm.disk :disk, size: "50GB", primary: true
    #  config.disksize.size = '50GB'
    config.vm.provider "virtualbox" do |vb|
        vb.name = "VPN Server - Ubuntu"
        vb.cpus = 2
        vb.memory = "4096"
    end
end