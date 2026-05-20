# FCOS - ISO

## Install
sudo loadkeys de
sudo coreos-installer install /dev/sda --ignition-url https://raw.githubusercontent.com/bellerG/coreos/refs/heads/main/config.ign
sudo reboot

- Login: core
- Passwort: welcome1

## Installs
sudo -i
rpm-ostree install tmux
rpm-ostree install -n fail2ban fail2ban-systemd nftables-services

systemctl reboot

rpm -q tmux fail2ban fail2ban-systemd nftables-services
rpm-ostree status


systemctl enable fail2ban.service
systemctl start fail2ban.service
systemctl status fail2ban.service
