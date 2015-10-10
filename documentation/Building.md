Building
==

## Buildroot

    
    $ cd CHIP-SDK
    $ vagrant up
    $ vagrant ssh
    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-buildroot
    vagrant@vagrant-ubuntu-trusty-32:~$ make chip_defconfig
    vagrant@vagrant-ubuntu-trusty-32:~$ make nconfig
    vagrant@vagrant-ubuntu-trusty-32:~$ make


[Flash C.H.I.P. from C.H.I.P. SDK! (Virtual Machine) ](https://nextthingco.zendesk.com/hc/en-us/articles/210864097-Flash-C-H-I-P-from-C-H-I-P-SDK-Virtual-Machine-)

### BuildRoot Copy

    vagrant@vagrant-ubuntu-trusty-32:~/CHIP-buildroot$ scp -r ../CHIP-buildroot/output/images/ xe1gyq@192.168.1.73:/home/xe1gyq/
    CHIP-tools/.firmware/images# 
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/rootfs.ubi .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sun5i-r8-chip.dtb .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sunxi-spl.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/u-boot-dtb.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/uboot-env.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/zImage .
    <Disconnect CHIP>
    <Connect CHIP>
    


## Chroot Debian Tree

http://www.raspibo.org/wiki/index.php/Chip9%24_How_to_install_a_chroot_Debian_tree
