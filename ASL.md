# Above Sea Level (ASL) Sensor

The pressure sensor, such as TGY-CAT01, can be configured
in the `System` ⭢ `Extra` ⭢ `ASL` menu:

![ASL Menu](asl.jpg)

The sensor cannot compute the altitude by itself, so the computation
is done inside the Tx firmware.

## Setup

The **default values** can be set by long pressing the `OK` button.

A short press of the `OK` button is used to change between the pressure
at the sea level and temperature. The Altitude is calculated as altitude
**above the sea level**.

To set the **relative altitude**, set a current pressure and temperature
at the start position.

Altitude is re-calculated on every value change.

