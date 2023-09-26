#python #virtualenviroment #virtualization 

---
> hun7er Cybersecurity | Sep 26th, 2023
---

# Pyenv Installation guide

Hello here you can find an ***installation guide*** to install `pyenv` and an example for the installation of `python v3.8.0` and the `dependencies` to solve the challenge `hashpump`.

---
#### Build Dependencies
<br />

Install all dependencies with the following command:
```shell
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```
---

#### Using the pyenv-installer
<br />

Curl's the `pyenv` installer and executing it with the following command:
```bash
curl https://pyenv.run | bash
```

<br />

Copy the following command to the end off your `.zshrc` file:
```bash
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```
---

#### Using pyenv to Install Python
<br />

List all available `python` version's in `pyenv` from `3.6.0` - `3.8.0`:
```bash
pyenv install --list | grep " 3\.[678]"
```

<br />

Install's `python v3.8.0` in `pyenv` with the following command:
```bash
pyenv install -v 3.8.0
```

<br />

Set `python v3.8.0` as global in `pyenv` with the following command:
```bash
pyenv global 3.8.0
```

* restart your ***terminal***

---

#### Control Dependencies
<br />

Install `g++` and `libssl-dev`  with the following command:
```bash
sudo apt-get install g++ libssl-dev -y
```

<br />

Install `hashpumpy` over `pip3` with the following command:
```bash
pip3 install hashpumpy
```
---

#### Reset Global Setting
<br />

Set `pyenv` back to `system` with the following command:
```bash
pyenv global system
```
---