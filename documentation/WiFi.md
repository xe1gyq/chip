# WiFi

    # connmanctl technologies
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
    # connmanctl enable wifi
    Enabled wifi
    # connmanctl scan wifi
    Scan completed for wifi
    # connmanctl services
        INFINITUMndjj        wifi_8c18d9f26f78_494e46494e4954554d6e646a6a_managed_psk
        INFINITUM8240C7      wifi_8c18d9f26f78_494e46494e4954554d383234304337_managed_psk
    # connmanctl connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Error /net/connman/service/wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk: Not registered


    # connmanctl
    connmanctl> agent on
    Agent registered
    connmanctl> connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Agent RequestInput wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
      Passphrase = [ Type=psk, Requirement=mandatory, Alternates=[ WPS ] ]
      WPS = [ Type=wpspin, Requirement=alternate ]
    Passphrase? 
    Connected wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    connmanctl> quit 
    # ifconfig


https://nextthingco.zendesk.com/hc/en-us/articles/209758368-Connecting-C-H-I-P-to-a-Wireless-Network