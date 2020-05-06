# FlyPlus: 14-Channel Firmware for FlySky i6

This is an alternative firmware for **FlySky i6** transmitters.
See below for the list of [features](#features) added
(including the [14 channels](14-channels) support, of course!)
and [hardware mods](#hardware-mods-supported) supported.

![Main Screen](main-screen-flyplus.jpg)


## Credits

The firmware is a modification of original FlySky firmware inspired
and based on work of _@ThomHpl_ and _Dave Borthwick_,
With use of repository created by
[@benb0jangles](https://github.com/benb0jangles/FlySky-i6-Mod-)
and input from _@povlhp_. Currently supported
and maintained by _@qba667_ with great input and improvements from _@Yenya_.

Including input from rcgroups users from the following thread:

[FlySky-FS-i6-8-channels-firmware-patch!](https://www.rcgroups.com/forums/showthread.php?2486545-FlySky-FS-i6-8-channels-firmware-patch!)

The Turnigy TGY-CAT01 support could be implemented by by courtesy of *inode_* - thanks for providing of the sensor and huge amount of measurement and analysis made by cookieqk.

In case if you want to support the project and reward me the time I spent on the FW please click this affiliate link when shopping at Banggood - It is free for you, but I will get reward from Banggood: 

https://www.banggood.com/?p=SB06021048261201501J

The project is Free Software and is made available free of charge. Your donation, which is purely optional.
If you like the software, you can also consider a donation.
All donations are greatly appreciated!

[![Donate](https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VSM36U6F7EN68)


## Features

* [Refined main screen](Main-Screen)
* [14 channels](14-channels) (channel 5-14 as auxilliary)
* [Extra Menu](Extra-Menu)
* [Configurable Tx battery voltage limit](Tx-Battery)
* [Pairs of switches](Switches-Combined) used together as a single channel
* [Flight timer](Timer)
* [Configurable telemetry alarms](Alarms)
* [Vario: accoustic altitude feedback](Vario)
	- using either TGY-CAT01 or [Arduino-based altitude sensor](https://github.com/Yenya/ibus-altitude-sensor) by @Yenya
* [ASL sensor](ASL), such as TGY-CAT01
* [PPM input](PPM-input) for custom channels
* [Configurable output of RX (PPM/PWM/SBUS/IBUS)](Rx-Output)
* [Telemetry](Telemetry) with more sensors supported and displayed
* [RSSI value sent to Rx](Get-RSSI-as-PPM-PWM-SBUS-IBUS) as a channel

## Hardware Mods Supported

* [Switch SwB modified for three positions](HW-Mod-SwB)
* [New switch SwE](HW-Mod-SwE)
* Potentiometer in place of switch SwC

## [How to Install this Firmware](Install)

## Tools

* GfxEditor
* Python scripts

## For Developers 

TODO
