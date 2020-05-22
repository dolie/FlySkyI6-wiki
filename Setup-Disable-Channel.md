# Disable the Channel Using a Switch

This is commonly requested feature for FlyPlus developers:

* [Aux = VRx\*SWy (Issue #64)](https://github.com/qba667/FlySkyI6/issues/64)
* [ Modify "Mix" so that a slave channels input can be held at zero (Issue #82)](https://github.com/qba667/FlySkyI6/issues/82)

But it can be done with standard FlySky firmware mixes.

## Setup

For example, let's assume that we want to configure enabling or disabling
of `VrA` potentiometer by a switch `SwA`.

Firstly, set up `VrA` as `Ch5`, and `SwA` as `Ch6`:

```
Key → Aux Channels
   Channel 5: VrA
   Channel 6: SwA
```

Then use one of the mixes as follows:

```
Key → Mix → Mix 1
   Mix is    On
   Master    Ch6
   Slave     Ch5
   Pos. mix  100%
   Neg. mix  100%
   Offset    -50%
```

