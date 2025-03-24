### Expand Ubuntu Disk Space in VMware Workstation

```bash

# Unmount Filesystems and Disable Swap
# Unmount all mounted partitions on /dev/sda
sudo umount /dev/sda1
sudo umount /dev/sda2
sudo umount /dev/sda3
# Disable swap (if it’s using /dev/sda)
sudo swapoff -a
# Verify that nothing is mounted
lsblk

# Proceed with fdisk
# Delete and Recreate the Partition
sudo fdisk /dev/sda
    d  # Press d and then 3 to delete /dev/sda3
    n  # Press n to create a new partition
       # Do you want to remove the signature? [Y]es/[N]o:  N

sudo reboot

# Resize the Filesystem
sudo resize2fs /dev/sda3

# Verify the Changes
df -h
```
