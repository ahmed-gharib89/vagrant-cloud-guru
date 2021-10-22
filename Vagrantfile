# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder "app/", "/var/www/app/", type: "rsync",
    create: true, owner: "vagrant", group: "vagrant",
    rsync__auto: true, id: "app"
end
