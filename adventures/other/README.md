### other linux adventure


##### `mkdir`
```bash
# Add -m to set permissions (e.g., 755):
# Add x: Creates parent directories if they don’t exist

mkdir -p -m 755 /path/to/dir
```

##### `PATH` environment variable
```bash
export PATH="$PATH:/opt/app/bin"
```

##### Screen Record in Linux
```bash
sudo apt install vokoscreen-ng
vokoscreenNG
```

#### Add user to sudoer
```bash
sudo visudo
# Add following line to the file
# your_username ALL=(ALL:ALL) ALL
```

#### jq
If you want to manipulate with json file, you can use jq command
```bash
sudo apt update
```
```bash
sudo apt install jq
```
```bash
jq '.' your_file.json
```
What about in Python?
```bash
python3 -m json.tool your_file.json
```

#### du
```
du -sh . --exclude='my-frontend' --exclude='.venv'
```
