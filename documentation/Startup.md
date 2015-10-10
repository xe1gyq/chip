# StartUp

## Host

    $ dmesg
    [35377.892165] usb 2-4.1: new high-speed USB device number 20 using ehci-pci
    [35377.984784] usb 2-4.1: New USB device found, idVendor=0525, idProduct=a4a7
    [35377.984787] usb 2-4.1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
    [35377.984790] usb 2-4.1: Product: Gadget Serial v2.4
    [35377.984792] usb 2-4.1: Manufacturer: Linux 4.2.0-rc1 with musb-hdrc
    [35377.994941] cdc_acm 2-4.1:2.0: This device cannot do calls on its own. It is not a modem.
    [35377.995007] cdc_acm 2-4.1:2.0: ttyACM0: USB ACM device
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
