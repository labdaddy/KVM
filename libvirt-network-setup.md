#### First and foremost. All credit due is given to the fine folks at Ubuntu for their KVM page on the Ubuntu help site. Check it out [here](https://help.ubuntu.com/community/KVM)
#### And also to the amazing work of Jamie Nguyen on the [Libvirt Networking Handbook](https://jamielinux.com/docs/libvirt-networking-handbook/#libvirt-networking-handbook) for transforming a frustrating, complicated subject into a clear, understandable and practical possibility! 




- Check network: `ip addr show virbr0`. This should show something like: 4: virbr0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default qlen 1000
    link/ether 52:54:00:32:7e:07 brd ff:ff:ff:ff:ff:ff
    inet 192.168.122.1/24 brd 192.168.122.255 scope global virbr0
       valid_lft forever preferred_lft forever
