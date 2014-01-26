netstat
=======

netstat command with process names in Android adb shell

If the uid is 0 or 1000, its process name will be 'system' and shared uid has many process names.

I have changed toolbox's netstat in Android source code(https://android.googlesource.com/platform/system/core/+/master/toolbox/netstat.c).
