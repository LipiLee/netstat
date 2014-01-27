netstat
=======

netstat command with process names in Android adb shell

If the uid is 0 or 1000, its process name will be 'system' and shared uid has many process names.

I have changed toolbox's netstat in Android source code(https://android.googlesource.com/platform/system/core/+/master/toolbox/netstat.c).

Proto Recv-Q Send-Q Local Address               Foreign Address             State       Process
 tcp       0      0 127.0.0.1:55555             0.0.0.0:*                   LISTEN      /system/bin/mediaserver
 tcp       0      0 127.0.0.1:55556             0.0.0.0:*                   LISTEN      /system/bin/mediaserver
 tcp       0      0 192.168.1.4:5070            0.0.0.0:*                   LISTEN      com.skt.rcs, com.skt.rcs:nable_isp
 tcp       0      0 192.168.1.4:38265           220.103.212.41:4081         ESTABLISHED com.skt.skaf.OA00199800
 tcp       0      0 192.168.1.4:58625           211.188.227.101:5071        ESTABLISHED com.skt.rcs, com.skt.rcs:nable_isp
tcp6       0      0 :::44523                    :::*                        LISTEN      com.sec.pcw
tcp6       0      0 :::16720                    :::*                        LISTEN      com.sec.pcw
tcp6       0      0 ::ffff:192.168.1.4:37953    ::ffff:74.125.128.113:443   ESTABLISHED com.google.process.gapps, com.google.process.location, com.google.android.gms
tcp6       0      0 ::ffff:192.168.1.4:54656    ::ffff:173.194.72.188:5228  ESTABLISHED com.google.process.gapps, com.google.process.location, com.google.android.gms
tcp6       0      0 ::ffff:192.168.1.4:56945    ::ffff:110.76.140.61:5228   ESTABLISHED com.kakao.talk
tcp6       1      0 ::ffff:192.168.1.4:42003    ::ffff:61.37.150.162:80     CLOSE_WAIT  system
tcp6       0      0 ::ffff:192.168.1.4:48146    ::ffff:74.125.128.95:443    ESTABLISHED com.google.process.gapps, com.google.process.location, com.google.android.gms
tcp6       0      0 ::ffff:192.168.1.4:56094    ::ffff:74.125.128.101:443   TIME_WAIT   system
tcp6       0      0 ::ffff:192.168.1.4:36918    ::ffff:74.125.128.156:80    TIME_WAIT   system
tcp6       0      0 ::ffff:192.168.1.4:48152    ::ffff:108.160.162.54:443   TIME_WAIT   system
tcp6       0      0 ::ffff:192.168.1.4:33355    ::ffff:175.158.4.235:5228   ESTABLISHED com.nhn.nni
tcp6       0      0 ::ffff:192.168.1.4:48157    ::ffff:108.160.162.54:443   ESTABLISHED com.dropbox.android
tcp6       0      0 ::ffff:192.168.1.4:53074    ::ffff:203.248.180.247:443  TIME_WAIT   system
tcp6       0      0 ::ffff:192.168.1.4:33146    ::ffff:14.63.224.94:80      ESTABLISHED com.sec.spp.push
tcp6       0      0 ::ffff:192.168.1.4:36924    ::ffff:74.125.128.156:80    TIME_WAIT   system
