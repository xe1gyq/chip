WiFi
==

## Buildroot

    root@chip:~# connmanctl technologies
    /net/connman/technology/bluetooth
      Name = Bluetooth
      Type = bluetooth
      Powered = False
      Connected = False
      Tethering = False
    /net/connman/technology/wifi
      Name = WiFi
      Type = wifi
      Powered = False
      Connected = False
      Tethering = False
    root@chip:~# connmanctl enable wifi
    Enabled wifi
    root@chip:~# connmanctl scan wifi
    Scan completed for wifi
    root@chip:~# connmanctl services
        INFINITUMndjj        wifi_8c18d9f26f78_494e46494e4954554d6e646a6a_managed_psk
        INFINITUM8240C7      wifi_8c18d9f26f78_494e46494e4954554d383234304337_managed_psk
    root@chip:~# connmanctl connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Error /net/connman/service/wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk: Not registered


    root@chip:~# connmanctl
    connmanctl> agent on
    Agent registered
    connmanctl> connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Agent RequestInput wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
      Passphrase = [ Type=psk, Requirement=mandatory, Alternates=[ WPS ] ]
      WPS = [ Type=wpspin, Requirement=alternate ]
    Passphrase? 
    Connected wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    connmanctl> quit 
    root@chip:~# ifconfig
    root@chip:~# ping -c 4 8.8.8.8
    PING 8.8.8.8 (8.8.8.8): 56 data bytes
    64 bytes from 8.8.8.8: seq=0 ttl=59 time=45.729 ms
    64 bytes from 8.8.8.8: seq=1 ttl=59 time=32.499 ms
    64 bytes from 8.8.8.8: seq=2 ttl=59 time=168.429 ms
    64 bytes from 8.8.8.8: seq=3 ttl=59 time=42.329 ms
    
    --- 8.8.8.8 ping statistics ---
    4 packets transmitted, 4 packets received, 0% packet loss
    round-trip min/avg/max = 32.499/72.246/168.429 ms
    root@chip:~# ifconfig
    lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
    wlan0     Link encap:Ethernet  HWaddr 8C:18:D9:F2:6F:78  
          inet addr:192.168.1.64  Bcast:192.168.1.255  Mask:255.255.255.0
              ...
    wlan1     Link encap:Ethernet  HWaddr 8E:18:D9:F2:6F:78  
          inet6 addr: fe80::8c18:d9ff:fef2:6f78/64 Scope:Link


[Connecting C.H.I.P. to a Wireless Network ](https://nextthingco.zendesk.com/hc/en-us/articles/209758368-Connecting-C-H-I-P-to-a-Wireless-Network)

## Debian


    root@chip:~# nmcli device wifi list
    *  SSID             MODE   CHAN  RATE       SIGNAL  BARS  SECURITY  
       INFINITUMfjph    Infra  1     54 Mbit/s  62      ▂___  WPA1 WPA2 
       INFINITUM8240C7  Infra  11    54 Mbit/s  55      ▂▄__  WPA1 WPA2 
       17057Abril       Infra  6     54 Mbit/s  50      ▂▄__  WPA1 WPA2 
       INFINITUMndjj    Infra  2     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUMf89t    Infra  9     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUM6d6f    Infra  4     54 Mbit/s  30      ▂___  WPA1 WPA2 
       --               Infra  1     54 Mbit/s  72      ▂▄▆_  --        
       INFINITUME75B40  Infra  6     54 Mbit/s  29      ▂___  WPA1 WPA2 
    
    *  SSID             MODE   CHAN  RATE       SIGNAL  BARS  SECURITY  
       INFINITUMfjph    Infra  1     54 Mbit/s  62      ▂___  WPA1 WPA2 
       INFINITUM8240C7  Infra  11    54 Mbit/s  55      ▂▄__  WPA1 WPA2 
       17057Abril       Infra  6     54 Mbit/s  50      ▂▄__  WPA1 WPA2 
       INFINITUMndjj    Infra  2     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUMf89t    Infra  9     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUM6d6f    Infra  4     54 Mbit/s  17      ▂___  WPA1 WPA2 
       --               Infra  1     54 Mbit/s  72      ▂▄▆_  --        
       INFINITUME75B40  Infra  6     54 Mbit/s  29      ▂___  WPA1 WPA2 
    root@chip:~# nmcli device wifi connect INFINITUMf password 1c28 ifname wlan0
    root@chip:~# nmcli device wifi connect INFINITUMf ifname wlan0
    Connection with UUID '...5d288d5d...' created and activated on device 'wlan0'
    root@chip:~# nmcli device status
    DEVICE   TYPE      STATE         CONNECTION    
    wlan0    wifi      connected     -- 
    wlan1    wifi      disconnected  --            
    ip6tnl0  ip6tnl    unmanaged     --            
    lo       loopback  unmanaged     --            
    sit0     sit       unmanaged     --            
    root@chip:~# nmcli connection show --active
    NAME           UUID                                  TYPE             DEVICE 
    --             dbdf4061-9b7f-4dc2-82aa-5d288d5d15f0  802-11-wireless  wlan0  
    root@chip:~# ping 8.8.8.8
    PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
    64 bytes from 8.8.8.8: icmp_seq=2 ttl=57 time=23.6 ms
    ^C
    --- 8.8.8.8 ping statistics ---
    2 packets transmitted, 1 received, 50% packet loss, time 1003ms
    rtt min/avg/max/mdev = 23.637/23.637/23.637/0.000 ms
    
- [Installing Zero Configuration Networking](https://nextthingco.zendesk.com/hc/en-us/articles/212946627-Installing-Zero-Configuration-Networking)


