#### Setup Virtual Machines In KVM
- virt-install --name {somenamehere}
- --memory {in MiB, like 2048}
- --vcpus {recommend only 1}
- --disk size= {no space between the = and the value, value is in GiB, like 80}
- -os-variant {windows10 or rhel8}
- --cdrom {for isos} {and then location such as} /home/username/Downloads/rhel8-iso

#### Sample Setup Values: 
virt-install --name demo-guest1 --memory 1024 --vcpus 1 --disk size=30 --os-variant win10 --cdrom /home/username/Downloads/Win10install.iso

### Running VM's In KVM
- using the `virsh start` utility: `virsh start` {vmname}
- Example: `virsh start rhel8iso`

### Checking Available VM's
- sudo `virsh list`

#### NOTE: for os-variant: KVM requires SUPER SPECIFIC naming for the os-variant. There is a list of oses that are recognized as valid names. View this list with: `osinfo-query os`. The resulting list is all the os names you can use in this field. Keep scrolling until you see your os name, then copy it with `ctrl+shift+c` and paste with `ctrl+shift+v`.
