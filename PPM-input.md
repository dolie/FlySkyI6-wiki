An external source of channel data can be connected to the trainer port on the back side of the transmitter (the PS/2 port)

<picture of trainer port and pinout>

The channels are then mapped to aux channels PPM4, PPM5, PPM6 which can be configured to real channels in the aux-channel assignment menu.
[[https://github.com/qba667/FlySkyI6/blob/master/doc/img/menu/model-setup/aux-channels.jpg|alt=Aux Channels]]

Configuration is possible for channels from original implementation (channels 5-6) as well as for channels 7-14.
In case of newer receivers PPM output is also active for channels 7-8. 
All configured values are also exposed as IBUS/SBUS values.

To configure channels 11-14 on Aux. channels page keep pressing "OK" button. 

Valid PPM input should contain 6 channels if 8 channels variant is being used channels 7-8 will overlap channels 1-2.
