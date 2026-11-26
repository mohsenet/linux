### Repai FireFox

```bash
sudo snap remove --purge firefox
```
```bash
sudo systemctl restart snapd snapd.socket
```
```bash
sudo apt install firefox
```
```bash
sudo kill -9 187924
sudo killall apt apt-get
```
```bash
sudo dpkg --configure -a
```
```bash
sudo add-apt-repository ppa:mozillateam/ppa

echo 'Package: firefox*
Pin: release o=LP-PPA-mozillateam
Pin-Priority: 1001' | sudo tee /etc/apt/preferences.d/mozilla-firefox

sudo apt update
sudo apt install -t 'o=LP-PPA-mozillateam' firefox
```
