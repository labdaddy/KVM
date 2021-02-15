#### Proxmox first setup
After installation is complete we need to update. We are using the free community version of Proxmox so we need to change the default enterprise software repository to the free community one.
- Click the name of your server
- Then click `shell` over on the right
- Then type all of the following:
- `cd /etc/apt/sources.list.d
mv pve-enterprise.list pve-enterprise.list.disabled
echo 'deb http://download.proxmox.com/debian/pve buster pve-no-subscription' > pve-community.list
apt update
apt -y dist-upgrade`
- Then reboot
- All done.
