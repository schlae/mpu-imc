# Roland MPU-IMC Clone

**Warning: There is not enough information in this repository to build your
own card. The microcontroller, IC3, has not been dumped, and the logic in
the gate array chip, IC2, is unknown.**

Based on information available in the MPU-IMC service manual, here is an
exact copy of the board layout. The MIDI Processing Unit is a way to connect
digital musical instruments to a computer using the IBM MCA bus.

Further details on the card are available [here](http://ohlandl.ipv7.net/sound/Roland_MPU-IMC.html).

There are two versions of this board in this repository. The first is a clone
of the stock MPU-IMC. The second is a version that incorporates the circuitry
of the external breakout box normally required for the MPU-IMC, including
the optocoupler required by the MIDI specification.

If you're not sure which board you want to build, choose the modified card.
It has several advantages:

1. You will not need the external Roland breakout box.
2. You can use the card bracket from a common IBM token-ring network card.
3. The DE-9 connector uses the more common footprint.

There are some important caveats with this board set:

1. IC2, the HG62E08, is a gate array chip customized by Roland. Think of it
like a small CPLD but hard coded in ROM. I have no information on the internal
schematic. Beware: not all HG62E08 parts will implement the same exact functions.
Look for a Roland house part number, and make sure they match.
2. IC3, the HD6801VD855P, is a custom mask-programmed microcontroller that
runs the whole show. I have no ROM for this microcontroller.
Before paying for expensive PC boards, make sure you have these chips first!
2. **Neither of these boards have been fabricated or tested. Do so at your
own risk.**

For fabrication, use a 2-layer process. I prefer getting a 30-degree edge bevel,
but that's up to you. Technically you should get hard gold for the edge fingers,
but that's usually expensive and immersion gold works just fine.

## MPU-IMC (Plain)

Following are reference materials for your convenience.

[Schematic](https://github.com/schlae/mpu-imc/blob/master/StockCard/RolandMpuImc.pdf)

[Bill of materials](https://github.com/schlae/mpu-imc/blob/master/StockCard/RolandMpuImc.csv)

[Fab files](https://github.com/schlae/mpu-imc/raw/master/StockCard/fab/RolandMpuImc.zip)

**Please note that the DE-9 connector is NOT the standard connector commonly
available**--the distance between the mounting holes and the front plane of
the connector is somewhat larger than usual. You may have to search surplus
sources to find one that will fit, or modify the footprint.

## MPU-IMC (Modified)

Following are reference materials for your convenience.

[Schematic](https://github.com/schlae/mpu-imc/blob/master/ModdedCard/RolandMpuImcMod.pdf)

[Bill of materials](https://github.com/schlae/mpu-imc/blob/master/ModdedCard/RolandMpuImcMod.csv)

[Fab files](https://github.com/schlae/mpu-imc/raw/master/ModdedCard/fab/RolandMpuImcMod.zip)

The DE-9 connector uses the industry standard footprint and is readily available from Mouser.
It's been relocated so that the card bracket from an IBM token ring network card (74F9321)
will fit.

# License

This work is licensed under a Creative Commons Attribution 4.0 International License. See [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

