Vagrant.require_version '>= 1.8.5'

Vagrant.configure('2') do |config|
    config.hostmanager.enabled = true
    config.hostmanager.manage_host = true
    config.hostmanager.manage_guest = true

    config.vm.provider :virtualbox do |v|
        v.customize [
            'modifyvm', :id,
            '--name', 'provision-vm',
            '--cpus', 1,
            '--memory', 1024,
            '--natdnshostresolver1', 'on',
            '--nictype1', 'virtio',
            '--nictype2', 'virtio',
        ]
    end

    config.vm.define 'provision-vm' do |node|
        node.vm.box = 'ubuntu/xenial64'
        node.vm.network :private_network, ip: '192.168.21.21', nic_type: 'virtio'
        node.vm.hostname = 'provision.dev'
    end
end
