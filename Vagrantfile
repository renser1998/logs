Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
    config.vm.box_version = "2004.01"
    config.vm.provider :virtualbox do |v|
      v.memory = 512
      v.cpus = 1
    end
  
    boxes = [
      {
        name: "web",
        ip: "192.168.56.110",
        playbook: "playbooks/web.yaml",
      },
      {
        name: "log",
        ip: "192.168.56.111",
        playbook: "playbooks/log.yaml",
      },
    ]
  
    boxes.each do |opts|
      config.vm.define opts[:name] do |config|
        config.vm.hostname = opts[:name]
        config.vm.network "private_network", ip: opts[:ip]
        config.vm.provision :ansible do |ansible|
          ansible.playbook = opts[:playbook]
        end
      end
    end
  end