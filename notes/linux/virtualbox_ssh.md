Set up SSH on a VirtualBox vm

## Setup
Power off the vm.

On the host run:
```
VBoxManage modifyvm vm_name --natpf1 "ssh,tcp,,3022,,22"
```

On the vm run:
```
sudo apt-get install openssh-server
sudo ufw allow 22
```

## To connect
On the host run:
```
ssh -p 3022 user@127.0.0.1
```
