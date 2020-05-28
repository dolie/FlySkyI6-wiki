# Aileron Differential

## Purpose

When the ailerons are controlled by two servos, using two independent
receiver channels can yield better results than plugging both servos to the
same channel using an Y-cable.

Firstly, the **differential**, i.e. the larger travel in the upwards
direction than in the downwards direction can be set up. It can of course,
be also set up mechanically by offset of the servo rods, but setting this
up inside the Tx can get more flexibilty. See [this article](https://www.rc-airplane-world.com/aileron-differential.html)
for more in-depth explanation.

Apart from that, both ailerons can be set up to move down or up simultaneously,
providing **flaperons** or **spoilerons**, respectively. For full-span
ailerons, both options can be used. However, *never configure flaperons
for partial-span ailerons*: it can easily lead to loss of control at low
speed!


## Set up

Plug the right aileron to `Ch1`, and the left aileron to `Ch5`.
Assign the `VrA` potentiometer to `Ch5`. This is what will be used to control
the simultaneous up or down movement of the ailerons (of course, it is
possible to use `SwC` instead):

```
Key → Aux Channels
   Channel 5: VrA
```

Then configure the end points to provide bigger travel upwards than
downwards:

```
Key → End points
   Ch1   75%  100%
   ...
   Ch5  100%   75%
```

Copy the `Ch1` to `Ch5`:

```
Key → Mix → Mix #1
   Mix is     On
   Master     Ch1
   Slave      Ch5
   Pos. mix   100%
   Neg. mix   100%
   Offset       0%
```

Allow adjustments of `Ch1` with the `Ch5` potentiometer:

```
Key → Mix → Mix #2
   Mix is     On
   Master     Ch5
   Slave      Ch1
   Pos. mix   -66%
   Neg. mix   -50%
   Offset       0%
```

And finally, modify the adjustments of `Ch5` by the potentiometer on `Ch5`:
```
Key → Mix → Mix #3
   Mix is     On
   Master     Ch5
   Slave      Ch5
   Pos. mix   -33%
   Neg. mix   -50%
   Offset       0%
```

