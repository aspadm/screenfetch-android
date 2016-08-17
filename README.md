# screenfetch-android

This program is analogue of screenfetch.

After starting, print Android logo and some system information.

Example:

........╲▂▃▄▄▄▃▂╱..........root@degas3g

.......▄▇███████▇▄.........(Aspadm@android-tablet)

......▌██▃█████▃██▌........OS: Android 4.4.2 KitKat (API 19)

......█████████████........Kernel: armeabi-v7a Linux 3.10.0-6131520

..▆█▆.▆▆▆▆▆▆▆▆▆▆▆▆▆.▆█▆....Uptime: 5h 18m

..███.█████████████.███....Packages: 189

..███.█████████████.███....Busybox: 1.24.1

..███.█████████████.███....Device: samsung SM-T231

..███.█████████████.███....Resolution: 800 x 1280

......█████████████........Launcher: ZenUI Launcher

........███...███..........Chipset: mrvl PXA1088

........███...███..........CPU:  PXA1L88 (4) @1183MHz

........███...███..........Memore: 804MB / 1289MB



usage: sfa <-hctsv>
 h - show help (this message)
 v - show version and exit
 c - also take screenshot (need root)
 s - show system info with simple no utf8 logo
 t - as is prev, but without color (simple text)


example: sfa -tc - show textual sysinfo and take 2 screenshot to your /sdcard
         sfa     - just show sysinfo (with colored utf8 logo)

Dependings:
terminal emulator
root access - for correct work (launcher detect) and for screenshots
toolbox (android contains it default)
