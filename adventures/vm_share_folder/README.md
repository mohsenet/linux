
## shared folders are not visible after reboot

### Before you do that
```bash
# ensure the following folder is exist
sudo mkdir -p /mnt/hgfs/
```

### manualy fix problem
```bash
sudo /usr/bin/vmhgfs-fuse .host:/ /mnt/hgfs/ -o subtype=vmhgfs-fuse,allow_other
```

# automatically fix problem
```bash
# edit /etc/fstab and add an entry to mount the Shared Folders automatically on boot.
# For example, add the line:
vmhgfs-fuse /mnt/hgfs fuse defaults,allow_other 0 0
```

### for test:
```bash
sudo umount /mnt/hgfs
sudo mount -a
ls /mnt/hgfs/
```
