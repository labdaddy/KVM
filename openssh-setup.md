### OpenSSH setup
- Install openssh: `sudo yum –y install openssh-server openssh-clients`
- To start ssh: `sudo systemctl start sshd`
- To check ssh status: `sudo systemctl status sshd`
- To stop ssh: `systemctl stop sshd`
- To enable ssh to start automatically after each system reboot by using the systemctl command: `sudo systemctl enable sshd`
- To disable ssh persistence after reboot enter: `sudo systemctl disable sshd`
##### Create a hosts file so you dont have to enter IP addresses every time
- Change to ssh directory: `cd .ssh`
- Open vi and add the host data:
- `vi config`
- `Host server1`
- `HostName [ip address]`
- `User root`
- `Port 22`
- Then save and exit


##### Ssh server configuration is needed to harden server security. The most common settings to enhance security are changing the port number, disabling root logins, and limiting access to only certain users. To edit these settings access the /etc/ssh/sshd_config file: `sudo vim /etc/ssh/sshd_config`
##### Disabling root logins and editing the default port number are good places to start.
- Disable root login: `PermitRootLogin no`
- Change the SSH port to run on a non-standard port. For example: `Port 2002`
##### Save the file after edits and restart sshd: `service ssh resart`

- To access a remote host type: `ssh ipaddress` or `ssh username@ipaddress`.
- Logging in to a remote machine with `ssh ipaddress' the remote machine will assume you intend to use the same username you are currently logged in as.
- Logging in as `ssh username@ipaddress` you will be prompted for the password of the user you are attempting to login as.

##### Key based authentication is even more secure than logging in with passwords and should be setup right away.
- Generate a public key on the first server: `ssh-keygen -t rsa`. This creates an RSA type public key to share with the remote server.
- The system  will prompt for a passphrase which should be different than any password used on either system.
- Verify key has been created: `cd .ssh`
- List the contents of the ssh directory: `cd .ssh` then `ls`
- Should show this: id_rsa id_rsa.pub known_hosts
