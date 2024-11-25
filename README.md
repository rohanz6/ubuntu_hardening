# ubuntu_hardening
### Adding a user to the sudo group
```bash
sudo adduser newuser
sudo usermod -aG sudo newuser
```
### Disabling and removing unwanted services
```bash
sudo systemctl disable cups-browsed
sudo apt autoremove cups-daemon
sudo systemctl disable avahi-daemon
sudo apt purge avahi-daemon
```
### Enabling and configuring UFW (Uncomplicated Firewall)
```bash
sudo ufw enable
sudo ufw default deny incoming
sudo ufw default deny forward
sudo ufw default allow outgoing
```

### Masking ctrl-alt-del to prevent shutdown via keyboard shortcut
```bash
sudo systemctl mask ctrl-alt-del.target
sudo systemctl daemon-reload
```
### Checking SSH status and removing SSH if necessary
```bash
sudo systemctl status ssh
sudo apt remove openssh-server openssh-client
sudo apt autoremove
```
### Locking root account and disabling login
```bash
sudo usermod -s /sbin/nologin root
clear
sudo passwd -l root
```
### Configuring SSH settings
```bash
sudo nano /etc/ssh/sshd_config
sudo systemctl restart ssh
```
### Updating and upgrading packages
```bash
sudo apt update && sudo apt dist-upgrade -y
sudo apt autoremove
sudo apt update && sudo apt dist-upgrade -y
```
### Installing security tools
```bash
sudo aa-status
sudo apt install apparmor-profiles apparmor-utils
sudo aa-enforce /etc/apparmor.d/*
```
### Installing and using Firejail for browser sandboxing
```bash
sudo apt install firejail -y
sudo firejail firefox
```
### Installing and running RKHunter for rootkit scanning
```bash
sudo apt install rkhunter -y
sudo rkhunter -c
```
### Installing system monitoring tools
```bash
sudo apt install htop neofetch
```
### Antivirus for Linux
### Install and Configure fail2ban
### Remove Unnecessary Packages
### Remove Unnecessary Services
### Automatic Update, Upgrade






























