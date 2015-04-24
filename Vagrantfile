# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "hashicorp/precise32"

    config.vm.network :public_network

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
        ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    end
    config.ssh.forward_x11 = true
end
