## virtualization
Virtualization tips, tricks and gotchas 
### First. The virtualization stack looks like this:
Virtualization api (libvirt) running on top of:
Hardware virtualization assistant (KVM) running on top of a:
Hypervisor (QEMU) running on top of:
Physical machine (that you are sitting at right now)

### Virtualization in more detail
**Libvirt** is a virtualization api that allows the user to access the virtual machines in an easy GUI interface or throught the command line. It provides all of the higher level features.
**KVM** is a hardware virtualization assistant that creates a digital replica of the actual physical machine (the host) and makes it possible to run many versions of that digital copy concurrently. The digital copies are called virtual machines. Resources on the actual physical machine (host) can be allocated to virtual machines (VMs) at will up to the maximum resources actually available on the host machine. Having digital copies of the physical hardware is awesome because different operating systems can be installed in these copies (guests) and still run on the same physical machine. A linux host could run windows and macos and even other versions of linux in these VMs all at the same time or any other combination thereof.
**QEMU** is a hypervisor 

#### To setup a virtualized network on the local host will require a bunch of steps.

1. Install and setup KVM - see separate instructions at KVM-setup
2. Setup networking in libvirt - see separate instructions at libvirt-network-setup
3. Install and setup openssh - see separate instructions at openssh-setup
4. Have fun !
