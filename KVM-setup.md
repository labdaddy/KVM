### KVM Setup
1. First check to make sure the processor supports virtualization: `lscpu | grep Virtualization`
Should return something like: VT-x
2. Update the system
3. Install virtualization packages:
#### Ubuntu: `sudo apt-get install qemu-system-x86 qemu-kvm qemu libvirt-bin virt-manager virtinst bridge-utils cpu-cjecker virt-viewer`
#### Centos: `yum install virt-manager libvirt libvirt-python python-virtinst`
-Alternate (needs verification) yum install kvm qemu-kvm qemu-img virt-manager libvirt libvirt-python libvirt-client virt-install virt-viewer bridge-utils-
- Start and enable the libvirt service: `systemctl start libvirtd` enter then `systemctl enable libvirtd`
- Make sure KVm is loaded: ` lsmod | grep kvm`
- In the case of using a minimal installation you will need the x-window package because virt-manager wont start: `yum install "@X Window System" xorg-x11-xauth xorg-x11-fonts-* xorg-x11-utils -y`
- Start virt-manager: `virt-manager`
