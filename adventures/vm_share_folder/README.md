
# shared folders are not visible after reboot

### Before you do that
```bash
sudo apt install open-vm-tools-desktop

# If you're in a server environment
sudo apt install open-vm-tools 

# After installation, restart the VMware Tools service
sudo systemctl restart open-vm-tools
sudo systemctl status open-vm-tools

# ensure the following folder is exist
sudo mkdir -p /mnt/hgfs/
```

### manualy fix problem
```bash
sudo /usr/bin/vmhgfs-fuse .host:/ /mnt/hgfs/ -o subtype=vmhgfs-fuse,allow_other
```

### automatically fix problem
```bash
# edit /etc/fstab and add an entry to mount the Shared Folders automatically on boot.
# For example, add the line:
vmhgfs-fuse /mnt/hgfs fuse defaults,allow_other 0 0
```

### for test
```bash
sudo umount /mnt/hgfs
sudo mount -a
ls /mnt/hgfs/
```
