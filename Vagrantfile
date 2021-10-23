# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder "app/", "/var/www/app/",
    create: true, owner: "vagrant", group: "vagrant",
    id: "app"
  config.vm.network "forwarded_port", guest: 8080, host: 8081,
    auto_correct: true, id: "wandrer-app"
end
