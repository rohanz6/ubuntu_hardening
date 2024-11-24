# ubuntu_hardening
### Adding a user to the sudo group
sudo adduser exb
sudo usermod -aG sudo exb

### Disabling and removing unwanted services
sudo systemctl disable cups-browsed
sudo apt autoremove cups-daemon
sudo systemctl disable avahi-daemon
sudo apt purge avahi-daemon

### Enabling and configuring UFW (Uncomplicated Firewall)
sudo ufw enable
sudo ufw default deny incoming
sudo ufw default deny forward

### Masking ctrl-alt-del to prevent shutdown via keyboard shortcut
sudo systemctl mask ctrl-alt-del.target
sudo systemctl daemon-reload

### Checking SSH status and removing SSH if necessary
sudo systemctl status ssh
sudo apt remove openssh-server openssh-client
sudo apt autoremove

### Locking root account and disabling login
sudo usermod -s /sbin/nologin root
clear
sudo passwd -l root

### Configuring SSH settings
sudo nano /etc/ssh/sshd_config
sudo systemctl restart ssh

### Updating and upgrading packages
sudo apt update && sudo apt dist-upgrade -y
sudo apt autoremove
sudo apt update && sudo apt dist-upgrade -y

### Installing Firefox and security tools
sudo apt install firefox
sudo aa-status
sudo apt install apparmor-profiles apparmor-utils
sudo aa-enforce /etc/apparmor.d/*

### Installing and using Firejail for browser sandboxing
sudo apt install firejail -y
sudo firejail firefox

### Installing and running RKHunter for rootkit scanning
sudo apt install rkhunter -y
sudo rkhunter -c

### Installing system monitoring tools
sudo apt install htop neofetch
neofetch
































