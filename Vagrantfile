VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "heroku/trusty64"

  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provision 'ansible' do |ansible|
    ansible.sudo = true
    ansible.playbook = 'nginx.yml'
  end
end
