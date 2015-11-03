# SandBox

http://www.instructables.com/id/Turn-your-Raspberry-Pi-into-a-Portable-Bluetooth-A/
https://wiki.archlinux.org/index.php/Bluetooth#Configuration_via_the_CLI

    # top
    Mem: 34452K used, 468024K free, 88K shrd, 0K buff, 8148K cached
    CPU:   0% usr   0% sys   0% nic  99% idle   0% io   0% irq   0% sirq
    Load average: 0.00 0.01 0.05 1/48 179
      PID  PPID USER     STAT   VSZ %VSZ %CPU COMMAND
      179   163 root     R     2092   0%   0% top
      120     1 root     S     5944   1%   0% /usr/sbin/connmand -n
      121     1 root     S     5748   1%   0% /usr/sbin/wpa_supplicant -u
      138     1 root     S     4348   1%   0% /usr/sbin/sshd
      162     1 root     S     3676   1%   0% /usr/libexec/bluetooth/bluetoothd
      101     1 dbus     S     2232   0%   0% dbus-daemon --system
      163     1 root     S     2092   0%   0% -sh
      164     1 root     S     1992   0%   0% /sbin/getty -L tty0 115200 vt100
      161     1 root     S     1992   0%   0% /sbin/getty -L ttyS0 115200 vt100
        1     0 root     S     1988   0%   0% init
       83     1 root     S     1988   0%   0% /sbin/syslogd -n
       85     1 root     S     1988   0%   0% /sbin/klogd -n
      156     1 root     S     1408   0%   0% /sbin/rtk_hciattach -n -s 115200 /dev/
       66     2 root     SW       0   0%   0% [kworker/u2:4]
       20     2 root     SW       0   0%   0% [kworker/0:1]
       12     2 root     SW       0   0%   0% [kdevtmpfs]
       70     2 root     SW       0   0%   0% [ubi_bgt0d]
        7     2 root     SW       0   0%   0% [rcu_sched]
       18     2 root     SW<      0   0%   0% [bioset]
       21     2 root     SW       0   0%   0% [kswapd0]

