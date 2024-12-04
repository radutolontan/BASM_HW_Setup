# BASM_HW_Setup
Repository describing setup procedure for MCUs used for BASM exhibits

# Raspberry Pi
1. Update Raspberry Pi OS 
```bash
sudo apt-get update
```
```bash
sudo apt-get upgrade
```
```bash
sudo reboot
```

2. Configure the static ipV4 connection
```bash
sudo nmcli con add type ethernet con-name <PiLAN> ifname eth0
```
```bash
sudo nmcli con modify <PiLAN> ipv4.method manual ipv4.addresses <172.16.17.11>
```
, where ```<PiLAN>``` and ```<172.16.17.11>``` can be replaced with any other connection name and static ipV4 address respectively

3. Follow [instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to setup an SSH Key to access repositories from GitHub.
4. Follow [instructions](https://code.visualstudio.com/docs/remote/ssh) to setup the SSH Server on the Pi. This will enable an SSH Client to use VSCode to read / write local files on the Pi for code development.