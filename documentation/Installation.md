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

https://nextthingco.zendesk.com/hc/en-us/articles/210863457-Installing-C-H-I-P-SDK-

    Install VirtualBox 4.3

https://github.com/NextThingCo/
