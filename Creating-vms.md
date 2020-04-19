#### Creating VM's in KVM/ libvirt

- virt-install --name {whatever you want to call your server}\
- --memory {in MiB, like 2048}\
- --vcpus {recommend only 1 unless very heavy load is expected}\
- --disk size=20 {no space between the = and the value, value is in GiB, like 80}\
- -os-variant {win10 or rhel8}\
- --cdrom {for isos} {and then location such as} /home/username/Downloads/rhel8-iso\

#### NOTE: for os-variant: KVM requires SUPER SPECIFIC naming for the os-variant. There is a list of oses that are recognized as valid names. View this list with: osinfo-query os. The resulting list is all the os names you can use in this field. Keep scrolling until you see your os name, then copy it with highlight and ctrl+shift+c.
