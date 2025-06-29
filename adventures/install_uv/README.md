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

If `uv version` not work, use following command.
```bash
mkdir -p ~/.local/bin
curl -LsSf https://astral.sh/uv/install.sh  | sh
# downloading uv 0.7.16 x86_64-unknown-linux-gnu
# no checksums to verify
# installing to /home/mohsen/.local/bin
#  uv
#  uvx
# everything's installed!

ls ~/.local/bin/uv
# /home/mohsen/.local/bin/uv

echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
vi .bashrc 
 
source ~/.bashrc
```

#### In Windows
```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### In MacOS
```bash
brew install uv
```
