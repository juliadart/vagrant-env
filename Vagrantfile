
Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  # Once the server has booted, run the following shell script
  config.vm.provision :shell, :path => 'provision.sh'

  # Mongo DB Ports
  config.vm.network :forwarded_port, host: 27017, guest: 27017
  config.vm.network :forwarded_port, host: 27018, guest: 27018
  config.vm.network :forwarded_port, host: 27019, guest: 27019
  config.vm.network :forwarded_port, host: 28017, guest: 28017

  # Sinatra Port
  config.vm.network :forwarded_port, host: 4567, guest: 4567

  # Shares the app folder
  config.vm.synced_folder "apps", "/home/vagrant/apps/"

  # Flask Port
  config.vm.network :forwarded_port, host: 5000, guest: 5000

  # Jenkins Port
  config.vm.network :forwarded_port, host: 8080, guest: 8080
end
