## A Virtual Machine for Mystand team
### Requirements
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

### Getting started
After installation of VirtualBox and Vagrant you need to execute next code

```
git clone git@github.com:mystand/mystand-dev-box.git
cd mystand-dev-box
```

Then you need to move your Vagrantfile.example to Vagrantfile.
Change F:/work/projects of Vagrantfile to destination to your shared folder
```
config.vm.synced_folder "F:/work/projects", "/home/vagrant/projects", type: "smb"
```

After changes execute `vagrant up`. That's all!

### What's In The Box
* RVM
* NVM
* Git
* SQLite3, MySQL, Postgres, MongoDB
* Elasticsearch
* Redis

Some usefull command for vagrant:
`vagrant up` - Start VM
`vagrant halt` - Shutdown VM
`vagrant reload --provision` - Reload all configuration of the Vagrantfile. 
