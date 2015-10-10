Installation
==

https://nextthingco.zendesk.com/hc/en-us/categories/200881468-C-H-I-P-

    # apt-get update
    # sudo apt-get install u-boot-tools android-tools-fastboot git build-essential libusb-1.0-0-dev
    $ git clone http://github.com/linux-sunxi/sunxi-tools
    $ cd sunxi-tools
    $ make
    # ln -s $PWD/fel /usr/local/bin/fel
    # cd .. 
    # git clone http://github.com/NextThingCo/CHIP-tools 
    # cd CHIP-tools
    # sudo ./chip-update-firmware.sh
    ...
    Contents:
       Image 0: 848 Bytes = 0.83 kB = 0.00 MB
    == upload the SPL to SRAM and execute it ==
    == upload images ==
    == execute the main u-boot binary ==

    $ cu -l /dev/ttyACM0 -s 115200


## At CHIP

    # hwtest

    ############################################################
    # [ CHIP HW TEST ]                                         #
    ############################################################
    
    # Turn on wlan0...OK
    # Turn on wlan1...OK
    # Hardware list...OK      
    # I2C bus 0...OK
    # I2C bus 1...OK
    # I2C bus 2...OK
    # testing AXP209 on I2C bus 0...OK
    # GPIO expander test...OK
    # Doing 10s stress test...OK
    # Wifi enumeration test...OK
    ### ALL TESTS PASSED ###


https://nextthingco.zendesk.com/hc/en-us/articles/210863457-Installing-C-H-I-P-SDK-

## CHIP SDK

### Install VirtualBox 4.3
    
    # nano /etc/apt/sources.list
    deb http://download.virtualbox.org/virtualbox/debian vivid contrib
    # cd
    # wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | apt-key add -
    # apt-get update
    # apt-get install virtualbox-5.0
    # apt-get install dkms

### Install VirtualBox Extension Pack 4.3

http://download.virtualbox.org/virtualbox/4.3.30/Oracle_VM_VirtualBox_Extension_Pack-4.3.30-101610.vbox-extpack

### Install Vagrant

    # apt-get install install vagrant


### Install Git

    # apt-get install git


### Virtual Machine Startup

    $ cd CHIP-SDK
    $ vagrant up
    $ vagrant ssh
    vagrant@vagrant-ubuntu-trusty-32:~$ 
    vagrant@vagrant-ubuntu-trusty-32:~$ ./CHIP-SDK/setup_ubuntu1404.sh


## Issues

    # usermod -a -G dialout vagrant
    # adduser vagrant dialout
    # chmod 666 /dev/ttyACM0
    # cu -l /dev/ttyACM0 -s 115200


- http://pastebin.com/w5pDhHAe
- https://github.com/NextThingCo/
- https://bbs.nextthing.co/t/unable-to-flash-alpha-c-h-i-p/544/41
