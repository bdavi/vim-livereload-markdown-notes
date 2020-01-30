Set up SSH on a VirtualBox vm

## Setup
On the vm:
```
VBoxManage modifyvm vm_name --natpf1 "ssh,tcp,,3022,,22"
```

On the host:
```
sudo apt-get install openssh-server
```

## To connect
Run on the host:
```
ssh -p 3022 user@127.0.0.1
```
