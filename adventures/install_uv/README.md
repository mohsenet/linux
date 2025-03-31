### install uv (UltraViolet)


#### In Ubuntu
```bash
sudo apt install curl
curl -LsSf https://astral.sh/uv/install.sh | sudo sh
# For regular user's PATH ==> for example mohsen user
curl -LsSf https://astral.sh/uv/install.sh | sh

# Reopen your terminal and run following command
uv version
```

#### In Windows
```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### In MacOS
```bash
brew install uv
```
