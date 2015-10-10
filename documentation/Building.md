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

    $ scp -r ../CHIP-buildroot/output/images/ xe1gyq@192.168.1.73:/home/xe1gyq/

## Chroot Debian Tree

http://www.raspibo.org/wiki/index.php/Chip9%24_How_to_install_a_chroot_Debian_tree
