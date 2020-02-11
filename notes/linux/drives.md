## List Drives
```
sudo fdisk -l
```

## Create Mount Point
First create folder to mount:
```
mkdir /home/mount_here
```

Then mount:
```
sudo mount dev/sdb1 /home/mount_here
```

Add `-t` to specify type (i.e. ext4)

## Unmount
```
sudo umount dev/sdb1
```
