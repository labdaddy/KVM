#### Create a new disk and add it to a virtual machine 
- Shut down the virtual machine in question
- Re locate to the standard disk storage location: `cd /var/lib/libvirt/images`
- Create a new disk with this compound command: Use elevated priveleges, state the type of storage (qemu-img), then create a disk image, then name the disk, then select the amount of disk space you want to add in M or G:
`sudo qemu-img create -f raw mynewdisk 1G`
-Another option is to create a qcow disk with: `sudo qemu-img create -f qcow2 mynewdisk 1G`. This option is better for VM's because you can easily use it for snapshots and such.
- Check your work: `ls -lh`. The new disk should be visible
Now we want to attach the disk to the virtual machine
- Check for the name of the current disk so we know what to attach to: `df`
- Now attach the new disk: `virsh attach-disk vm-name /var/lib/libvirt/images/img-name vdb --cache none
- Or use: 
- ` virsh attach-disk vm-name \`
- `--source /var/lib/libvirt/images/img-name \`
- `--target vdb \`
- `--persistent`

Example: attach the disk image ‘/var/lib/libvirt/images/mynewdisk‘ as a virtio disk to the VM/domain named ‘ubuntu-box1‘ and update the domain xml file for new disk (type command on the host):
$ sudo virsh attach-disk mynewdisk /var/lib/libvirt/images/ubuntu-box1-vm-disk1-5G vdb --cache none
