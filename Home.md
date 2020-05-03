# FlyPlus: 14-Channel Firmware for FlySky i6

This is an alternative firmware for FlySky i6 transmitters.
See below for the list of features added (including the 14 channels
support, of course!).

## [How to install this firmware](Install.md)

## Features

* [Configurable flight timer](Timer.md)

* [Configurable telemetry alarms](Alarms.md)

* Configurable battery 

* Basic telemetry from RX (RSSI, Nosie, SNR)

* Advanced Telemetry
There is also version sending IBus channel data and telemetry on same wire (serial port):

https://github.com/qba667/MAVLinkToIbus/tree/master/IA6B


* Configurable output of RX (PPM/PWM/SBUS/IBUS) 

* [3 positions Switch B](HW-Mod-SwB.md)

* [2 positions Switch E added](HW-Mod-SwE.md)

* Variable in place of Switch C

* Using PPM input for custom channels

* Refined main screen

* Channels 12-14 sendinng PPM values 6,5,4 (in older version)

* RSSI (Error) send on channel 11 (in older version)

* Handling AC frames (up to 28 bytes)

## Tools

* Updater by ThomHpl
* Updater by mhils
* GfxEditor
* Python scripts

## Developers 

## Telemetry protocol

## Credits

The firmware is a modification of oryginal FlySky firmware inspired
and based on work of @ThomHpl and Dave Borthwick. With use of repository
created by @benb0jangles and input from @povlhp. Currently supported
and maintained by @qba667 with great input and improvements from @Yenya.

Including input from rcgroups users from thread: https://www.rcgroups.com/forums/showthread.php?2486545-FlySky-FS-i6-8-channels-firmware-patch!

The Turnigy TGY-CAT01 could be implemented by by courtesy of inode_ - thanks for providing of the sensor and huge amount of measurement and analysis made by cookieqk.

In case if you want to support the project and reward me the time I spent on the FW please click this affiliate link when shopping at Banggood - It is free for you, but I will get reward from Banggood: 

https://www.banggood.com/?p=SB06021048261201501J

The project is Free Software and is made available free of charge. Your donation, which is purely optional.
If you like the software, you can also consider a donation.
All donations are greatly appreciated!

[![Donate](https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VSM36U6F7EN68)

