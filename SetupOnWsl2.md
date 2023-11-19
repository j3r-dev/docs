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

- Install Golang

[Golang installation guide](https://go.dev/doc/install)

Add in ~/.bashrc
```
# go
export PATH=$PATH:/usr/local/go/bin
```

- [Install NVM](https://github.com/nvm-sh/nvm#install--update-script)
- [Docker sans DockerDesktop](https://blog.lecacheur.com/2021/11/23/docker-sous-windows-wsl-2-sans-docker-desktop/)
