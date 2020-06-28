- Create a Default storage pool. The “default” storage pool for guest disks is “/var/lib/libvirt/images”. This is fine for test purposes, but if you have another mount that you want to use for guest OS disks, then you should create a custom storage pool. Commands to create a “kvmpool” on an SSD mounted at “/data/kvm/pool”:
- `virsh pool-list --all`   
 - `virsh pool-define-as kvmpool --type dir --target /data/kvm/pool`
 - Should return: `Pool kvmpool defined`
 - `virsh pool-list --all`
 - `virsh pool-start kvmpool`
 - `virsh pool-autostart kvmpool`
 - `virsh pool-list --all`
 - Should return: 
 Name                 State      Autostart 
-------------------------------------------
 default              active     yes 
 kvmpool              active     yes
