# ubuntu_hardening
'''
sudo adduser exabee
sudo usermod -aG sudo exabee

sudo systemctl disable cups-browsed
sudo apt autoremove cups-daemon
sudo systemctl disable avahi-daemon
sudo apt purge avahi-daemon
sudo ufw enable
sudo ufw default deny incoming
sudo ufw default deny forward
sudo systemctl mask ctrl-alt-del.target
sudo systemctl daemon-reload
sudo systemctl status ssh
sudo apt remove openssh-server openssh-client
sudo apt autoremove
sudo usermod -s /sbin/nologin root
clear
sudo passwd -l root
sudo nano /etc/ssh/sshd_config
sudo systemctl restart ssh
sudo apt update && sudo apt dist-upgrade -y
sudo apt autoremove
sudo apt update && sudo apt dist-upgrade -y
sudo apt install firefox
sudo aa-status
sudo apt install apparmor-profiles apparmor-utils
sudo aa-enforce /etc/apparmor.d/*
sudo apt install firejail -y
firejail firefox
sudo firejail firefox
firejail firefox
clear
sudo apt install rkhunter -y
sudo rkhunter -c
opensnitch
htop
sudo apt install htop
neofetch
sudo apt install neofetch
neofetch
'''

































