Debian
==

    root@chip:~# apt-get update
    root@chip:~# apt-get upgrade
    root@chip:~# dpkg-reconfigure tzdata # TimeZone
    root@chip:~# apt-get install xfce4
    root@chip:~# apt-get install -f
    root@chip:~# df -h
    Filesystem      Size  Used Avail Use% Mounted on
    ubi0:rootfs     3.6G  563M  3.1G  16% /
    devtmpfs        245M     0  245M   0% /dev
    tmpfs           246M     0  246M   0% /dev/shm
    tmpfs           246M  6.6M  239M   3% /run
    tmpfs           5.0M     0  5.0M   0% /run/lock
    tmpfs           246M     0  246M   0% /sys/fs/cgroup
    tmpfs            50M     0   50M   0% /run/user/0
    root@chip:~# apt-get install libasound2 alsa-utils
    root@chip:~# alsamixer