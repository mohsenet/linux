### Update
```bash
# update
sudo apt update
# Packages can be upgraded
apt list --upgradable
# To update all the packages
sudo apt upgrade
# to upgrade a specific package
sudo apt install --only-upgrade google-chrome-stable
```

### Remove the Problematic Repositories
```bash
sudo rm /etc/apt/sources.list.d/UBUNTU_REPOSITORY.list
```

### Force APT to re-download missing/corrupted packages
```bash
# sudo apt clean
# sudo apt update
# sudo apt upgrade

sudo apt upgrade --fix-missing
```
