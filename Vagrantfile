
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provision "shell", inline: <<-SHELL
     sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt xenial-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
     wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
	 apt-get update
     apt-get install -y postgresql-8.4
   SHELL
end
