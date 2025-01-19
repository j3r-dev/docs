- Install Windows Subsystem for Linux from Microsoft Store
- Install Debian from Microsoft Store
- Test version
```
wsl -l -v
```
- Run
```
sudo apt update
sudo apt full-upgrade
sudo apt install nano wget curl build-essential bash-completion ca-certificates zip git
```

- Browser settings

[Install wslu](https://wslutiliti.es/wslu/install.html)
Then add in `~/.bashrc`:
```
export BROWSER=wslview
```

- Install ASDF
[ASDF installation guide](https://asdf-vm.com/guide/getting-started.html)

python fix:
```
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl git \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

- Install Golang

[Golang installation guide](https://go.dev/doc/install)

Add in ~/.bashrc
```
# go
export PATH=$PATH:/usr/local/go/bin
```

- [Install NVM](https://github.com/nvm-sh/nvm#install--update-script)
- [Install PyEnv]([DOCKER_IMAGE](https://github.com/pyenv/pyenv#automatic-installer)
- [Docker sans DockerDesktop](https://blog.lecacheur.com/2021/11/23/docker-sous-windows-wsl-2-sans-docker-desktop/)


#### Launch Edge navigator from WSL (Deprecated cf Browser settings)
If the different command lines (like **aws sso login**) don't open automatically your windows navigator your could try the following:

1. Under a windows terminal
```cmd
cd c:\users\YOUR_LOGIN
mklink browser.exe "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe"
```

2. Under your WSL environment install xdg-utils
```bash
sudo apt install xdg-utils -y
# adapt YOUR_LOGIN with your own
echo export BROWSER="/mnt/c/Users/YOUR_LOGIN/browser.exe" >> ~/.bashrc
source ~/.bashrc
```
