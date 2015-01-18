VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "services" do |services|
    services.vm.box_url = "http://static.inputrequired.org/phpbnl15/dockerworkshop-phpbnl15-services.box"
    services.vm.box = "phpbnl15-services"
    services.ssh.forward_agent = true
    services.vm.network :private_network, ip: "33.33.33.30"
    services.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "512"]
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    services.vm.synced_folder "./", "/vagrant", disabled: true
  end

  config.vm.define "playground" do |playground|
    playground.vm.box_url = "http://static.inputrequired.org/phpbnl15/dockerworkshop-phpbnl15-playground.box"
    playground.vm.box = "phpbnl15-playground"
    playground.ssh.forward_agent = true
    playground.vm.network :private_network, ip: "33.33.33.31"
    playground.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "512"]
        vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    playground.vm.synced_folder "./", "/vagrant", disabled: true
  end

end