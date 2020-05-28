# Paraglide/Paramotor Setup

![Paraglide Servos](paraglide-servos.jpg)

## Paraglide Servos

The basic paraglide control uses two servos, each of them pulling its own side
of the brake lines (the rearmost lines). In the neutral position, the servo
levers ("hands") are both in the upmost position. When turning, only one of
the servos should pull its brake lines, i.e. the hand is going down.
This is unlike the V-Tail or Elevon mix, where *both* servos move
in the opposite directions during turns. When braking, both hands should
go down simultaneously.

The main challenge with setting this up is to use the full range of the servo
travel, instead of just half range. In other words, we want the servos
to be at one end of its travel when the sticks are in the neutral position.


## Paraglide Control Modes

There are two different ways how to pilot the paraglide:

* **Aileron-elevator control**, where the aileron direction controls
the left servo only when the stick is moved to the left, and the right servo
only when the stick moved to the right. In addition to that,
pulling the elevator direction pulls both servos simultaneously,
and pushing the elevator does nothing.

* **Full-scale control**, where the left stick from the neutral to the
outwards left position controls the full travel of the left servo,
the right stick from the middle to the outwards right position controls the
right servo, inwards movement of those sticks does nothing, and also
the elevator direction movement does nothing. This simulates how full-scale
paraglider pilots control the brake lines.

So far I did not find a good way how to set up the first mode with full servo
travel using only three available mixes of FS-i6. So I will describe how to
set up the second (full-scale like) type control:

## Setup (Full-scale Control)

I presume Mode 2 (throttle+rudder on the left stick) here. Plug the left servo
to `Ch4` and the right servo to `Ch1` of your receiver. Then set up the
following mixes in order to map half of the stick travel to the full travel
of the servos:

```
Key → Mix → Mix #1
   Mix is    On
   Master    Ch1
   Slave     Ch1
   Pos. mix  100%
   Neg. mix    0%
   Offset    -50%

Key → Mix → Mix #2
   Mix is    On
   Master    Ch4
   Slave     Ch4
   Pos. mix    0%
   Neg. mix  100%
   Offset    +50%
```

![Paraglide in Flight](paraglide-flight.jpg)


## Other Features

Some paraglides have additional servo(s) to control the A-lines (front lines).
Also, some pilots use potentiometer for controlling the neutral position
of the main servos, allowing them to fly in a _slightly braked_ mode.
So far I did not configure any of these features.

