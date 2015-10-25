Debian
==

## First Steps

    root@chip:~# apt-get update
    root@chip:~# apt-get upgrade
    root@chip:~# apt-get install wget htop mplayer
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
    
## Audio

sunxi-codec as hardware
    
    root@chip:~# aplay -lL
    ...
    **** List of PLAYBACK Hardware Devices ****
    card 0: sunxicodec [sunxi-codec], device 0: CDC PCM Codec-0 []
      Subdevices: 1/1
      Subdevice #0: subdevice #0
    root@chip:~# arecord -lL
    ...
    **** List of CAPTURE Hardware Devices ****
    card 0: sunxicodec [sunxi-codec], device 0: CDC PCM Codec-0 []
      Subdevices: 1/1
      Subdevice #0: subdevice #0

    root@chip:~# arecord -f cd -D plughw:0,0 -d 20 test.wav
    Recording WAVE 'test.wav' : Signed 16 bit Little Endian, Rate 44100 Hz, Stereo
    ^CAborted by signal Interrupt...
    root@chip:~# aplay -D hw:0,0 test.wav
    Playing WAVE 'test.wav' : Signed 16 bit Little Endian, Rate 44100 Hz, Stereo

### Testing

    chip@chip:~$ wget -O test.wav https://upload.wikimedia.org/wikipedia/commons/d/db/Descending_thirds.wav
    root@chip:~# apt-get install mplayer
    chip@chip:~$ wget -O test.ogg https://upload.wikimedia.org/wikipedia/commons/e/e7/Agogo.ogg
    chip@chip:~$ mplayer test.ogg
    chip@chip:~$ wget -O test.mp3 http://www.freesound.org/data/previews/315/315618_2050105-lq.mp3
    chip@chip:~$ mplayer test.mp3
    
- [Next Thing Co. Sound Output on Debian ](https://nextthingco.zendesk.com/hc/en-us/articles/212946707-Sound-Output-on-Debian)


## First Steps

    root@chip:~# apt-get update
