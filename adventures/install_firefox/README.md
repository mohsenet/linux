

### Download firefox
[Download](https://www.mozilla.org/en-US/firefox/new/)

### Install
```bash
cd ~/Downloads
tar -xf firefox-136.0.tar.xz

# Move the extracted firefox directory to a suitable location, such as /opt:
sudo mv firefox /opt/

sudo vi /usr/share/applications/firefox.desktop
```
### Add the following content to the file:
```ini
[Desktop Entry]
Name=Firefox
Exec=/opt/firefox/firefox
Icon=/opt/firefox/browser/chrome/icons/default/default128.png
Type=Application
Categories=Network;WebBrowser;
```

```bash
# Create a Symbolic Link (Optional)
sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox

# /opt/firefox/firefox
firefox

sudo update-alternatives --install /usr/bin/x-www-browser x-www-browser /opt/firefox/firefox 200
sudo update-alternatives --config x-www-browser

# Remove old firefox if exist
sudo apt remove firefox
```
