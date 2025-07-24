# Distrobox Installation Guide

First of all you need docker, here's the installation method that I use:
```bash
sudo pacman -S docker
```
After installation try `docker info` if you got permission denied, you may need to do this
```bash
sudo usermod -aG docker $USER
sudo chown "$USER":"$USER" /var/run/docker.sock   
```

Now, let's begin distrobox installation e.g I want to install `ubuntu:latest` version on my arch linux.
```bash
sudo pacman -S distrobox
distrobox create -n ubuntu --image ubuntu:latest
```
After installation done, let's enter our ubuntu system with `distrobox enter ubuntu`
```bash
Starting container...                   	 [ OK ]
Installing basic packages...   
```
Wait until the installation complete, and let's continue to the next step. To enter the distribution named `ubuntu` you can do this:
```bash
distrobox enter ubuntu
```
And now, let's try to do update & upgrade, if it's working then you already on ubuntu linux distribution cuz as you may know that apt command not available on arch linux.
```bash
sudo apt update && sudo apt upgrade
```
