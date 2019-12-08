Vagrant.configure("2") do |config|
  config.vm.box = "centos/8"
  config.vm.host_name = "nginx"
  config.vm.box_version = "1905.1"
  config.vm.provision "shell", inline: <<-SHELL
    mkdir -p ~root/.ssh; cp ~vagrant/.ssh/auth* ~root/.ssh
    sed -i '65s/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config
    systemctl restart sshd
  SHELL
end