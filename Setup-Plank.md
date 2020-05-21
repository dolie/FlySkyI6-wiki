# Plank Flying Wing

## Purpose

Flying wings have, of course, two *elevons*. Planks (flying wings without
the wing sweep) are a bit special in being extremely sensitive to the
elevator input, and a bit less sensitive to the aileron input.

I also wanted to have *flying modes* on a three-position switch:

* fast mode, elevator trimmed for fast flight
* slow mode, both elevons a bit raised, usable for slowly flying e.g. in thermals
* start mode, with elevons even more up

My plank wing is pretty aerobatic, and I tend to overcontrol it when flying
high in thermals. So I decided to use a previously unused rudder stick
as another, low-rate, aileron input.
 
## Setup

Plug elevon servos to `Ch1` and `Ch2`, respectively. Firstly set up the elevon
mmode:

```
Key → Elevon
   Elevon: On
   CH1: 100 %
   CH2: 50 %
```

Put a three-position switch `SwC` on `Ch5`:

```
Aux Channels → Channel 5: SwC
```

Use the mix to move the elevator up with `SwC`:

```
Mix → Mix 1
   Mix is     On
   Master     Ch5
   Slave      Ch2
   Pos. mix   -9 %      # Start/landing
   Neg. mix   -6 %      # Slow/thermal mode
   Offset     -3 %      # This must be half of the neg. mix
```

And finally, use the rudder stick as low-rate ailerons:

```
Mix → Mix 2
   Mix is     On
   Master     Ch4
   Slave      Ch1
   Pos. mix   50 %
   Neg. mix   50 %
   Offset      0 %
```

