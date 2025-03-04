## Set date and time to English

### Adjust your system's locale settings
```bash
# Check Current Locale Settings
locale
# Look for the LANG, LC_TIME, and LC_ALL variables. 

# Change Locale to English
sudo nano /etc/default/locale

# Modify the file to set the locale to English (e.g., en_US.UTF-8):
# LANG=en_US.UTF-8
# LC_TIME=en_US.UTF-8

# Generate Locales (if necessary)
sudo locale-gen en_US.UTF-8
sudo update-locale LANG=en_US.UTF-8 LC_TIME=en_US.UTF-8

# Verify the Changes
locale
```


