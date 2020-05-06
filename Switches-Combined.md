# Two Switches as a Single Channel #

Using this feature, it is possible to use *pairs* of switches
as a single channel source. Go to the `Key` ⭢ `Aux Channels` menu
to configure it. There are following combinations available:

* SwA+B
* SwB+C
* SwC+D

## 2-position and 3-position Switch ##

For the `SwA+B` and `SwC+D` variants, the channel value is computed as follows:

| SwA or SwD | SwB or SwC | Value   |
|------------|------------|---------|
|    off     |   0 (off)  | -100 %  |
|    off     |   1 (mid)  |  -60 %  |
|    off     |   2 (on)   |  -20 %  |
|    on      |   0 (off)  |   20 %  |
|    on      |   1 (mid)  |   60 %  |
|    on      |   2 (on)   |  100 %  |

The above assumes that the [three-position SwB switch](HW-Mod-SwB) has been
installed.

## Two 3-position Switches ##

For the `SwB+C` variant with [three-position SwB switch](HW-Mod-SwB)
the channel value is computed as follows:

| SwB        |  SwC       | Value   |
|------------|------------|---------|
| 0 (off)    |   0 (off)  | -100 %  |
| 0 (off)    |   1 (mid)  |  -75 %  |
| 0 (off)    |   2 (on)   |  -50 %  |
| 1 (mid)    |   0 (off)  |  -25 %  |
| 1 (mid)    |   1 (mid)  |    0 %  |
| 1 (mid)    |   2 (on)   |   25 %  |
| 2 (on)     |   0 (off)  |   50 %  |
| 2 (on)     |   1 (mid)  |   75 %  |
| 2 (on)     |   2 (on)   |  100 %  |

