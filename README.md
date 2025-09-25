# install_python_in_venv
This repository provides step-by-step instructions to install and use a specific Python version inside a virtual environment (venv) on Ubuntu.

# Steps:
## 1. Install Dependencies
```bash

sudo apt update
sudo apt install -y build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev libffi-dev wget
```

## 2. Download & Compile a Specific Python Version
```bash

cd /tmp
wget https://www.python.org/ftp/python/3.13.7/Python-3.13.7.tgz
tar -xf Python-3.13.7.tgz
cd Python-3.13.7
./configure --enable-optimizations
make -j$(nproc)
sudo make altinstall
```
