# Timer #

The FlyPlus firmware supports a timer counting from the plane takeoff on,
or counting the time throttle was on only. The timer value is displayed
in the upper left corner of the main screen, and after the preconfigured
time limit is reached, the transmitter beeps:

![Main Screen](main-screen.jpg)

### Set-up ###

Go to the `System` ⭢ `Extra` ⭢ `Timer` menu, which looks like this:

![Timer Menu](timer.jpg)


#### Channel ####

The first row selects the **Channel** which triggers the timer.
Usually you should choose `Channel 3`, the throttle channel
(which displays on the screen with no space, so don't confuse it for
`Channel 13`!).


#### Value ####

Arrow should be pointing at Value. Press UP or DOWN to pick a stick value to trigger the alarm. The timer will start when the channel exceeds the number chosen. 1000 roughly correlates to the stick being all the way down or left, 1500 roughly correlates to center stick, and 2000 roughly correlates to stick fully up or right. Trims and subtrims will affect the exact stick location, and servo reverse will change threshold direction. The value 1250 shall be considered as correct one - the throttle stick which triggers the timer at about 1/4 throttle. 

Alternatively, it is possible to fine-tune the value to start counting as soon
as the ESC starts spinning the motor. If you often fly with very low throttle,
the value of 1250 is way too big. Yenya sets the treshhold between 1000 and 1100 for all his ESCs.

NOTE: The first time in FW < 1.7.2 the numbers are set they start at some really high number like 65,535 or something. Long hold OK and the value will be reset to zero. 
The you can increment up to the desired value. The numbers increment by 10 per up press.
When you have the desired number set, press OK.


#### Alarm ####

Arrow should be pointing at Alarm. Use UP or DOWN to choose a desired timer duration. 
Here again in FW < 1.7.2 the very first time you set the time, it starts at some really high number, and you just have to long hold OK and the value will reset to 00:00:00. The display is in HH:MM:SS, and changes by 10 seconds for each UP or DOWN press. When you have the desired run time entered long hold CANCEL to store. 

Then short press CANCEL several times to back out of all menus and return to the main flight display.

When your trigger channel exceeds the trigger threshold, the timer on the flight display will start counting up. When the counter reaches the preset time, the alarm will sound.

If you trigger the timer by accident before you are ready, long press on CANCEL to reset the timer to 00:00:00. If the trigger channel is below the threshold, the timer will stay at 00:00:00 until triggered. If the trigger channel is above the threshold, the timer will reset to 00:00:00 then start counting up again.

When the timer is counting up, a long press on OK will bring up the System/Settings menu and pause the timer. You can continue to fly as normal and the timer will be paused. When you press CANCEL, the flight display will return and the counter will start counting again.

Once the alarm time is reached, the radio will beep once approximately every two seconds. To silence the alarm, long press CANCEL, and the timer will reset to zero and the alarm will be silenced. If the trigger channel is above the threshold, the timer will immediately begin counting again, otherwise it will stay at 00:00:00 until the trigger channel is moved above the threshold.


#### Hold ####

