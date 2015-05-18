# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box     = 'azure'
  config.vm.box_url = 'https://github.com/msopentech/vagrant-azure/raw/master/dummy.box'

  config.ssh.username         = 'vagrant'
  config.ssh.private_key_path = File.expand_path('~/.ssh/azurevagrant.pem')

  config.vm.provider :azure do |azure|
    azure.mgmt_certificate = File.expand_path('~/.ssh/azurevagrant.pem')
    azure.mgmt_endpoint    = 'https://management.core.windows.net'
    azure.subscription_id  = 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX'

    azure.cloud_service_name = 'azurevagrant'
    azure.storage_acct_name  = 'azurevagrantstorage'
    azure.deployment_name    = 'azurevagrantdeployment'

    azure.vm_name     = 'azurevagrantsmall'
    azure.vm_image    = 'b39f27a8b8c64d52b05eac6a62ebad85__Ubuntu-14_04_2-LTS-amd64-server-20150506-en-us-30GB'
    azure.vm_size     = 'Small'
    azure.vm_location = 'North Europe'

    azure.ssh_port             = '22'
    azure.ssh_private_key_file = File.expand_path('~/.ssh/azurevagrant.pem')
    azure.ssh_certificate_file = File.expand_path('~/.ssh/azurevagrant.cer')

    azure.tcp_endpoints = '8000'
  end

  config.vm.provision 'shell', inline: 'echo OHAI'
end
