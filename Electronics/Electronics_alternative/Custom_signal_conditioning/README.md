## Signal conditioning board



The custom board was designed using Altium (the project can be viewed with a free license of the [Altium Designer Viewer](https://www.altium.com/altium-designer-viewer)). You can find the project [here](Altium_project).

A [bill of materials](Bill_of_materials) and a [schematic of the circuit](Circuit) were automatically generated with Altium.

##### Power supply

The power is supplied to by a 12 V power supply.

##### Inputs

For each laser diode:

- 3.3 V or 5 V TTL trigger signal
- 3.3 V or 5 V (>=1 kHz) PWM control signal (to set the power of the laser diode)

##### Output

For each laser diode:

- Out: the Out signal should be fed directly to the external input of the Thorlabs laser diode driver.
