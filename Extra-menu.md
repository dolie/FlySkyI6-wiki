Extra menu
===
[[https://github.com/qba667/FlySkyI6/blob/master/doc/img/menu/system/extra.jpg|alt=Extra]]

* Timer
* Alarm
* SwB+C
* Tx Bat
* Vario
* ASL
* Endpoints (on the second page)

ASL
---
Menu "system->Extra->ASL"
[[https://github.com/qba667/FlySkyI6/blob/master/doc/img/menu/system/extra/asl.jpg|alt=ASL]]

TX battery monitoring
---
Menu "system->Extra->Tx Bat"
[[https://github.com/qba667/FlySkyI6/blob/master/doc/img/menu/system/extra/tx-bat.jpg|alt=Tx Bat]]

Current firmware has no longer a battery gauge in the upper right corner, instead a voltage reading is being used.
It is possible to change voltage alarm threshold to any number, by going into Extra>TX Bat. 
The value can be adjusted to use 1S/2S LiPo batteries.
If you use NiCds or NiMH, you can lower the voltage threshold to whatever you feel is best.

Endpoints
---
Menu "system->Extra->Endpoints"
[[https://github.com/qba667/FlySkyI6/blob/master/doc/img/menu/system/extra/endpoints.jpg|alt=Endpoints]]

Three columns with subtrim and Endpoint settings for channel 7-14

The structure is the following:

`Channel 07 [Min limit][Subtrim][Max limit]`

`Channel 08 [Min limit][Subtrim][Max limit]`

`Channel 09 [Min limit][Subtrim][Max limit]`

`Channel 10 [Min limit][Subtrim][Max limit]`

`Channel 11 [Min limit][Subtrim][Max limit]`

`Channel 12 [Min limit][Subtrim][Max limit]`

`Channel 13 [Min limit][Subtrim][Max limit]`

`Channel 14 [Min limit][Subtrim][Max limit]`

Default values are set to (min = -100%, subtrim = 0, max = 100%);

Min, max and subtrim can be positive or negative there is no restriction - the only restriction is:
`Min < subtrim <max`


