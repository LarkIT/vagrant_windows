Vagrant.configure("2") do |config|
  config.vm.box = "StefanScherer/windows_2016_docker"
  config.vm.network "forwarded_port", guest_ip: "10.0.2.15", guest: 80, host: 8080
  config.vm.provision "shell", inline: 'powershell -f c:\vagrant\install_dockercompose.ps1'
  config.vm.provision "shell", inline: 'docker pull nanoserver/iis'
  config.vm.provision "shell", inline: 'docker run --name nanoiis2 -d -it -p 80:80 nanoserver/iis'

end
