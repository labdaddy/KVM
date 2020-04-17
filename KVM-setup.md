### KVM Setup
1. First check to make sure the processor supports virtualization: `lscpu | grep Virtualization`
Should return something like: VT-x
2. Update the system
3. Install virtualization packages:
Ubuntu: sudo apt-get install qemu-system-x86 qemu-kvm qemu libvirt-bin virt-manager virtinst bridge-utils cpu-cjecker virt-viewer
Centos: yum install kvm python-virtinst libvirt libvirt-python virt-manager qemu-kvm qemu-img libvirt libvirt-client libvirt-python
