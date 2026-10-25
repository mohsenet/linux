Create a credentials file (avoid writing the password in plaintext in fstab)
```bash
sudo vi /etc/smb-credentials
```

Enter the following content:
```text
username=user
password=password
```

Then tighten the permissions so that only root can read it:
```bash
sudo chmod 600 /etc/smb-credentials
```

Edit `/etc/fstab`
```bash
sudo vi /etc/fstab
```
```text
//192.168.1.39/ShareName  /mnt/file-server-it  cifs  credentials=/etc/smb-credentials,uid=1000,gid=1000,iocharset=utf8,nofail  0  0
```
---
Key parameters:

```credentials=...```: Reads the username and password, avoiding plaintext exposure

```uid=1000,gid=1000```: Ensures that the regular user taha has read and write permissions on the mounted files

```iocharset=utf8```: Prevents garbled characters in Chinese

```nofail```: Even if the network share is unreachable at boot, it will not prevent the system from starting (recommended, otherwise it may get stuck in the boot process)

---
Test the mount
```bash
sudo mount -a
```

In docker-compose.yml file
```yml
version: "3.8"

services:
  student:
    build: .
    env_file: .env
    container_name: student
    ...
    volume:
        - /mnt/SHARED_FOLDER:SHARED_FOLDER
```
