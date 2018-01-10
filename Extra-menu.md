Extra menu
===
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra.jpg|alt=Extra]]

Timer
---
Menu "system->Extra->Timer"
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra/timer.jpg|alt=Timer]]

Configuration:
Arrow should be pointing at Channel. Press UP or DOWN to pick a channel to use to trigger the timer. Usually you should chose Channel 3, the throttle channel (which displays on the screen with no space, so don't confuse it for Channel 13!) Press OK.

Arrow should be pointing at Value. Press UP or DOWN to pick a stick value to trigger the alarm. The timer will start when the channel exceeds the number chosen. 1000 roughly correlates to the stick being all the way down or left, 1500 roughly correlates to center stick, and 2000 roughly correlates to stick fully up or right. Trims and subtrims will affect the exact stick location, and servo reverse will change threshold direction. The value 1250 shall be considered as correct one - the throttle stick which triggers the timer at about 1/4 throttle. 
NOTE: The first time in FW < 1.7.2 the numbers are set they start at some really high number like 65,535 or something. Long hold OK and the value will be reset to zero. 
The you can increment up to the desired value. The numbers increment by 10 per up press.
When you have the desired number set, press OK.

Arrow should be pointing at Alarm. Use UP or DOWN to choose a desired timer duration. 
Here again in FW < 1.7.2 the very first time you set the time, it starts at some really high number, and you just have to long hold OK and the value will reset to 00:00:00. The display is in HH:MM:SS, and changes by 10 seconds for each UP or DOWN press. When you have the desired run time entered long hold CANCEL to store. 

Then short press CANCEL several times to back out of all menus and return to the main flight display.

Operation: 
In FW < 1.7.0:
You only get one timer setting to share among all model memories, so if different models require different times, you'll have to reset the timer for each model.
In FW >= 1.7.0:
Timer settings are no more shared between models.

When your trigger channel exceeds the trigger threshold, the timer on the flight display will start counting up. When the counter reaches the preset time, the alarm will sound.

If you trigger the timer by accident before you are ready, long press on CANCEL to reset the timer to 00:00:00. If the trigger channel is below the threshold, the timer will stay at 00:00:00 until triggered. If the trigger channel is above the threshold, the timer will reset to 00:00:00 then start counting up again.

When the timer is counting up, a long press on OK will bring up the System/Settings menu and pause the timer. You can continue to fly as normal and the timer will be paused. When you press CANCEL, the flight display will return and the counter will start counting again.

Once the alarm time is reached, the radio will beep once approximately every two seconds. To silence the alarm, long press CANCEL, and the timer will reset to zero and the alarm will be silenced. If the trigger channel is above the threshold, the timer will immediately begin counting again, otherwise it will stay at 00:00:00 until the trigger channel is moved above the threshold.


Alarm
---
Menu "system->Extra->alarm"
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra/alarm.jpg|alt=Alarm]]

Select measurement, greater or less than and finally the value to check.


SWB+C
---

ASL
---

TX battery monitoring
---
Menu "system->Extra->Tx Bat"
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra/tx-bat.jpg|alt=Tx Bat]]

Current firmware has no longer a battery gauge in the upper right corner, instead a voltage reading is being used.
It is possible to change voltage alarm threshold to any number, by going into Extra>TX Bat. 
The value can be adjusted to use 1S/2S LiPo batteries.
If you use NiCds or NiMH, you can lower the voltage threshold to whatever you feel is best.

Vario
---
Menu "system->Extra->Vario"
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra/vario.jpg|alt=Vario]]
Select measurement source and Gain

(Q: what does gain do?)


Endpoints
---
Menu "system->Extra->Endpoints"
[[https://github.com/unitware/FlySkyI6/blob/doc-feature-ppm/doc/img/menu/system/extra/endpoints.jpg|alt=Endpoints]]

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


