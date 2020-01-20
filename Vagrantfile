# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :mark8smtp01 do |mark8smtp01|
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
    config.vm.box = "centos/7"
    config.ssh.username = "vagrant"
    config.ssh.insert_key = false
    config.ssh.private_key_path = ["/home/marcos/.ssh/vagrant_rsa", "~/.vagrant.d/insecure_private_key"]
    mark8smtp01.vm.hostname = "mark8smtp01"
    mark8smtp01.vm.network :private_network, ip: "192.168.205.10"
    # mark8smtp01.vm.network :public_network, ip: "192.168.1.10", bridge: "wlo1"
    config.vm.provision "shell",
      path:"tools/provision.sh"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "/workspace/ansible/ansiblepb/role-cl-k8s.yml"
    end
  end
  config.vm.define :mark8swrk01 do |mark8swrk01|
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
    config.vm.box = "centos/7"
    config.ssh.username = "vagrant"
    config.ssh.insert_key = false
    config.ssh.private_key_path = ["/home/marcos/.ssh/vagrant_rsa", "~/.vagrant.d/insecure_private_key"]
    mark8swrk01.vm.hostname = "mark8swrk01"
    mark8swrk01.vm.network :private_network, ip: "192.168.205.11"
    # mark8swrk01.vm.network :public_network, ip: "192.168.1.103", bridge: "wlo1"
    config.vm.provision "shell",
      path:"tools/provision.sh"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "/workspace/ansible/ansiblepb/role-cl-k8s.yml"
    end
  end
  config.vm.define :mark8swrk02 do |mark8swrk02|
    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
    config.vm.box = "centos/7"
    config.ssh.username = "vagrant"
    config.ssh.insert_key = false
    config.ssh.private_key_path = ["/home/marcos/.ssh/vagrant_rsa", "~/.vagrant.d/insecure_private_key"]
    mark8swrk02.vm.hostname = "mark8swrk02"
    mark8swrk02.vm.network :private_network, ip: "192.168.205.12"
    # mark8swrk02.vm.network :public_network, ip: "192.168.1.12", bridge: "wlo1"
    config.vm.provision "shell",
      path:"tools/provision.sh"
    config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "/workspace/ansible/ansiblepb/role-cl-k8s.yml"
    end
  end
end
