Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"
  config.vm.synced_folder ".", "/vagrant"
  config.vm.network "forwarded_port", guest: 8080, host: 8000
  config.vm.network "forwarded_port", guest: 80, host: 8081
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/deploy.yml"
  end
end
