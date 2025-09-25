# install_python_in_venv
This repository provides step-by-step instructions to install and use a specific Python version inside a virtual environment (venv) on Ubuntu.
<br><br>

# Steps:
## 1. Update & Install Dependencies
```
sudo apt update
sudo apt install -y build-essential libssl-dev zlib1g-dev libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev libffi-dev wget
```
<br><br>

## 2. Download & Compile a Specific Python Version
```
cd /tmp
```
> `/tmp` is the temporary directory on Linux which clear automatically when the system reboots. We gonna download and compile files which we don't need them in far future.

<br>Replace `3.13.7` with the version you need:
Download and extract python
```
wget https://www.python.org/ftp/python/3.13.7/Python-3.13.7.tgz
tar -xf Python-3.13.7.tgz
```

<br>Compile and install the Python
```
cd Python-3.13.7
./configure --enable-optimizations
make -j$(nproc)
sudo make altinstall
```
> We use `make altinstall` instead of `make install` to avoid overwriting the system’s default `python3`.

<br><br>

## 3. Create a Virtual Environment
You can name your venv. Here i ues `myenv`.
```
python3.10 -m venv myenv
```
<br><br>

## 4. Activate the Environment
```
source myenv/bin/activate
```
<br><br>

## 5. Verify Python Version
```
python --version
```
<br><br>

## 6. Deactivate the Environment
```
deactivate
```
