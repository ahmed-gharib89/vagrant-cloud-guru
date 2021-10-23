# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.define "app" do |app|
    app.vm.synced_folder "app/", "/var/www/app/",
      create: true, owner: "vagrant", group: "vagrant",
      id: "app"
      app.vm.network "forwarded_port", guest: 8080, host: 8081,
      auto_correct: true, id: "wandrer-app"
  end

  config.vm.define "prom" do |prom|
    prom.vm.network "forwarded_port", guest: 9090, host: 9090,
      auto_correct: true, id: "prometheus"
  end

end
