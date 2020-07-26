

#### To setup a network of virtual machines on the local host will require a few steps.

1. Install and setup KVM - see separate instructions at [KVM-setup](KVM-setup.md)
2. Setup networking in libvirt - see separate instructions at [libvirt-network-setup](libvirt-network-setup.md)
3. Install and setup openssh - see separate instructions at [openssh-setup](openssh-setup.md)
4. Have fun !

#### The virtualization stack looks like this:
- libvirt (virtualization api) ==> kvm (hardware assist) ==> QEMU (hypervisor) ==> Machine (physical hardware)

##### More Detail
1. Libvirt is a virtualization API that manages the KVM hardware assistance software and the QEMU hypervisor to provide higher level functions such as storage and network management.
2. KVM is a kernel module that exposes the /dev/kvm interface that can be used to perform hardware-assisted virtualization. This enables virtual machines to leverage fast CPU instructions to perform virtualization.
3. QEMU is a hosted hypervisor that emulates physical hardware such as CPU and network interfaces.
QEMU+KVM (sometimes written as QEMU/KVM) is the use of KVM associated with QEMU. QEMU still emulates the hardware but also leverages KVM to execute the guest operating system.
4. Machine physical hardware
