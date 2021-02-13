## Install VMWare Player on Ubuntu 20
Install packages
- `sudo apt-get update`
- `sudo apt-get install wget gcc build-essential linux-headers-generic linux-headers-$(uname -r)`
Download VMWare Workstation Player
- `cd /tmp`
- `wget --user-agent="Mozilla/5.0 (X11; Linux x86_64; rv:75.0) Gecko/20100101 Firefox/75.0" https://www.vmware.com/go/getplayer-linux`
Next, run these commands to install VMWare Workstation Player
- `chmod +x getplayer-linux`
- `sudo ./getplayer-linux`
The installer will run in the background and after a little bit should display:
`Extracting VMware Installer…done.
Installing VMware Player 15.5.2
Configuring…
[######################################################################] 100%
Installation was successful.`
Then launch the graphical Workstation Player using the icon in the programs dashboard.
Accept the terms of use, say yes to updates, skip the license and press install.
