# -*- mode: ruby -*-
# vi: set ft=ruby :

# Define
VAGRANTFILE_API_VERSION = "2"
VM_HOSTNAME = "tmp01"
VM_BOX = "centos/7"
VM_PRIVATE_IP = "192.168.33.201"
VM_SHARED_SOURCE = "../../"
VM_SHARED_TARGET = "/share"

# Configure
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = VM_BOX
  config.vm.define :VM_HOSTNAME do |vm|
    vm.vm.hostname = VM_HOSTNAME
    vm.vm.network :private_network, ip: VM_PRIVATE_IP
    vm.vm.synced_folder VM_SHARED_SOURCE, VM_SHARED_TARGET, mount_options: ['dmode=777','fmode=777'],owner: 0,group: 0
  end
end
