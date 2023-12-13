### Install manually python 3.10.11 on root directory using wsl commands 
```markdown
# Installing Python 3.10.11 on WSL

Follow these steps to install Python 3.10.11 on Windows Subsystem for Linux (WSL).

## 1. Update Package List

Update the package list to ensure you have the latest information about available packages.

```bash
sudo apt update
```

## 2. Install Essential Packages

Install essential packages required for building Python.

```bash
sudo apt install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
```

## 3. Download Python 3.10.11 Source

Download the Python 3.10.11 source code from the Python website.

```bash
wget https://www.python.org/ftp/python/3.10.11/Python-3.10.11.tgz
```

## 4. Extract Source Code

Extract the downloaded source code.

```bash
tar -xf Python-3.10.11.tgz
```

## 5. Configure and Build

Change into the extracted directory, configure, and build Python.

```bash
1.  cd Python-3.10.11
2.  ./configure --enable-optimizations
3.  make -j$(nproc)
```

## 6. Install Python

Install Python into the system.

```bash
sudo make altinstall
```

Using `altinstall` is preferred over `make install` to avoid conflicting with the system Python.

## 7. Check Python Version

Verify that Python 3.10.11 is installed.

```bash
python3.10 --version
```

This should display the Python version you just installed.

## 8. Clean Up

You can remove the downloaded source code to free up space.

```bash
cd ..
rm -r Python-3.10.11 Python-3.10.11.tgz
```

Now, you have Python 3.10.11 installed on your WSL. You can use `python3.10` or `python3` to invoke this version.

### create virtual environment
```
 python3.10 -m venv env
```
activate virtual environment 
```
 source env/bin/activate
```
