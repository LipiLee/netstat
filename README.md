netstat
=======

netstat command with process names in Android adb shell

If the uid is 0 or 1000, its process name will be 'system' and shared uid has many process names.

I have changed toolbox's netstat in Android source code(https://android.googlesource.com/platform/system/core/+/master/toolbox/netstat.c).

shell@klteskt:/data/local/tmp $ ./netstat3
Proto Recv-Q Send-Q Local Address               Foreign Address             State       Process
 tcp       0      0 0.0.0.0:9058                0.0.0.0:*                   LISTEN      com.nhn.android.appstore
 tcp       0      0 42.23.10.57:5060            0.0.0.0:*                   LISTEN      system
 tcp       0      0 127.0.0.1:9050              0.0.0.0:*                   LISTEN      com.sec.msc.nts.android.proxy
 tcp       0      0 10.120.105.73:51823         223.62.225.40:443           ESTABLISHED com.google.android.googlequicksearchbox:interactor, com.google.android.googlequicksearchbox:search
 tcp       0      0 10.120.105.73:60543         192.168.141.229:4080        ESTABLISHED com.skt.skaf.OA00199800
 udp       0      0 42.23.10.57:5060            0.0.0.0:*                   CLOSE       system
tcp6       0      0 ::ffff:127.0.0.1:51728      :::*                        LISTEN      com.facebook.orca
tcp6       0      0 ::ffff:127.0.0.1:38110      :::*                        LISTEN      com.facebook.katana
tcp6       1      0 ::ffff:10.120.105.73:50693  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:43057  ::ffff:211.33.88.69:80      CLOSE_WAIT  com.skmc.okcashbag.home_google:remote, com.skmc.okcashbag.home_google
tcp6       1      0 ::ffff:10.120.105.73:40354  ::ffff:182.162.90.112:80    CLOSE_WAIT  com.samsung.android.internal.headlines
tcp6       1      0 ::ffff:10.120.105.73:50261  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:46943  ::ffff:54.230.183.15:80     CLOSE_WAIT  com.visionobjects.resourcemanager
tcp6       0      0 ::ffff:10.120.105.73:37500  ::ffff:110.76.143.211:5228  ESTABLISHED com.kakao.talk
tcp6       0      0 ::ffff:10.120.105.73:48014  ::ffff:149.154.171.5:443    ESTABLISHED org.telegram.messenger
tcp6       0      0 ::ffff:10.120.105.73:38773  ::ffff:173.252.88.78:443    ESTABLISHED com.facebook.katana
tcp6       0      0 ::ffff:10.120.105.73:59309  ::ffff:125.209.217.81:5223  ESTABLISHED com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:49097  ::ffff:211.33.88.69:80      CLOSE_WAIT  com.skmc.okcashbag.home_google:remote, com.skmc.okcashbag.home_google
tcp6      54      0 ::ffff:10.120.105.73:40100  ::ffff:182.162.202.142:443  CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:53632  ::ffff:101.79.247.160:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       0      0 ::ffff:10.120.105.73:42669  ::ffff:1.234.25.200:23018   ESTABLISHED kr.co.tictocplus
tcp6       1      0 ::ffff:10.120.105.73:48013  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:59962  ::ffff:54.192.181.76:80     CLOSE_WAIT  system
tcp6       1      0 ::ffff:10.120.105.73:53728  ::ffff:182.162.202.137:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       0      0 ::ffff:10.120.105.73:60166  ::ffff:64.233.188.188:5228  ESTABLISHED com.google.process.gapps, com.google.android.gms.persistent, com.google.android.gms
tcp6       1      0 ::ffff:10.120.105.73:41220  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:42363  ::ffff:101.79.247.160:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:58448  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6      32      0 ::ffff:10.120.105.73:58617  ::ffff:182.162.193.90:443   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       0      0 ::ffff:10.120.105.73:46615  ::ffff:23.23.235.156:443    ESTABLISHED com.starbucks.co
tcp6       1      0 ::ffff:10.120.105.73:58693  ::ffff:182.162.202.175:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6      38      0 ::ffff:10.120.105.73:54836  ::ffff:203.236.20.112:9443  CLOSE_WAIT  com.skt.pe.provider
tcp6       1      0 ::ffff:10.120.105.73:40305  ::ffff:216.58.220.225:80    CLOSE_WAIT  com.android.vending
tcp6       0      0 ::ffff:10.120.105.73:33258  ::ffff:173.252.88.78:443    ESTABLISHED com.facebook.orca
tcp6       0      0 ::ffff:10.120.105.73:44084  ::ffff:173.194.126.169:443  ESTABLISHED com.google.process.gapps, com.google.android.gms.persistent, com.google.android.gms
tcp6       1      0 ::ffff:10.120.105.73:55673  ::ffff:182.162.202.137:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:39707  ::ffff:211.33.88.69:80      CLOSE_WAIT  com.skmc.okcashbag.home_google:remote, com.skmc.okcashbag.home_google
tcp6       0      0 ::ffff:10.120.105.73:51918  ::ffff:223.62.225.39:443    ESTABLISHED com.google.process.gapps, com.google.android.gms.persistent, com.google.android.gms
tcp6       1      0 ::ffff:10.120.105.73:47219  ::ffff:211.33.88.69:80      CLOSE_WAIT  com.skmc.okcashbag.home_google:remote, com.skmc.okcashbag.home_google
tcp6       1      0 ::ffff:10.120.105.73:48960  ::ffff:216.58.220.225:80    CLOSE_WAIT  com.android.vending
tcp6       1      0 ::ffff:10.120.105.73:46225  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       0      0 ::ffff:10.120.105.73:45559  ::ffff:173.194.126.169:443  ESTABLISHED com.google.process.gapps, com.google.android.gms.persistent, com.google.android.gms
tcp6       1      0 ::ffff:10.120.105.73:36407  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:41818  ::ffff:182.162.202.158:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:43540  ::ffff:182.162.202.142:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:34763  ::ffff:101.79.247.160:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:56929  ::ffff:182.162.202.142:80   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       0      0 ::ffff:10.120.105.73:48975  ::ffff:52.68.186.227:5223   ESTABLISHED com.sec.spp.push
tcp6       1      0 ::ffff:10.120.105.73:38335  ::ffff:54.192.181.156:80    CLOSE_WAIT  com.samsung.android.internal.headlines
tcp6      54      0 ::ffff:10.120.105.73:37586  ::ffff:182.162.202.142:443  CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6       1      0 ::ffff:10.120.105.73:38389  ::ffff:182.162.193.90:80    CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6      32      0 ::ffff:10.120.105.73:52974  ::ffff:182.162.193.90:443   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni
tcp6      32      0 ::ffff:10.120.105.73:40246  ::ffff:182.162.193.90:443   CLOSE_WAIT  com.nhn.android.band, com.nhn.nni

