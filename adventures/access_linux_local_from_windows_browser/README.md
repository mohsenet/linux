## Open an SSH connection to `SERVER_IP` as `user`, and while it's open, forward my local port 8088 to `127.0.0.1:8088` on the server.

### In Linux
```bash
sudo apt update
```
```bash
sudo apt install openssh-server
```
```bash
sudo systemctl status ssh
```

### In Powershell
```bash
ssh -L 8088:127.0.0.1:8088 taha@10.122.96.184
```

### In your Windows browser, go to"
```bash
http://localhost:8088
```

### Visualizing the path
```text
Windows browser          SSH tunnel (encrypted)            Ubuntu server
┌───────────────┐                                      ┌────────────────────┐
│ localhost:8088│ ──── ssh -L 8088:127.0.0.1:8088 ───► │ 127.0.0.1:8088     │
└───────────────┘                                      │ (your app/service) │
                                                       └────────────────────┘
```

