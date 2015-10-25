Image Custom
==

## Vagrant Up

    
    $ cd CHIP-SDK
    $ vagrant up
    $ vagrant ssh

## Buildroot & Debian

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-buildroot
    vagrant@vagrant-ubuntu-trusty-32:~$ make chip_defconfig
    ...
    # configuration written to /home/vagrant/CHIP-buildroot/.config
    ...
    vagrant@vagrant-ubuntu-trusty-32:~$ make nconfig
    vagrant@vagrant-ubuntu-trusty-32:~$ make
    vagrant@vagrant-ubuntu-trusty-32:~$ ls /home/vagrant/CHIP-buildroot/.config

### BuildRoot Flash, Old Method

### BuildRoot Copy, Old Method

    vagrant@vagrant-ubuntu-trusty-32:~/CHIP-buildroot$ scp -r ../CHIP-buildroot/output/images/ xe1gyq@192.168.1.73:/home/xe1gyq/
    # cd CHIP-tools/.firmware/images
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/rootfs.ubi .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sun5i-r8-chip.dtb .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sunxi-spl.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/u-boot-dtb.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/uboot-env.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/zImage .
    <Disconnect CHIP>
    <Connect CHIP>
    # cd CHIP-tools
    CHIP-tools$ ./chip-update-firmware.sh
    CHIP-tools$ cu -l /dev/ttyACM0 -s 115200
    <To Validate>
    # cd ~/CHIP-tools
    # BUILDROOT_OUTPUT_DIR=../CHIP-buildroot/output ./chip-fel-flash.sh


## Chroot Debian Tree

- [Flash C.H.I.P. from C.H.I.P. SDK! (Virtual Machine) ](https://nextthingco.zendesk.com/hc/en-us/articles/210864097-Flash-C-H-I-P-from-C-H-I-P-SDK-Virtual-Machine-)
- [Free Electrons Buildroot Training ](http://free-electrons.com/doc/training/buildroot/buildroot-slides.pdf)
- http://www.raspibo.org/wiki/index.php/Chip9%24_How_to_install_a_chroot_Debian_tree
