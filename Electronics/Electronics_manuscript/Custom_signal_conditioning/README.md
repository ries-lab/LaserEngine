## Voltage conditioning board



We produced two versions of the voltage conditioning board (A and B) with different voltage divider circuits, corresponding either the 405 nm and 488 nm (A) or the 638 nm (B)  laser diodes.

The custom board was designed using Altium (the project can be viewed with a free license of the [Altium Designer Viewer](https://www.altium.com/altium-designer-viewer)). You can find the project [here](Altium_project).

A [bill of materials](Bill_of_materials) and a [schematic of the circuit](Circuit) were automatically generated with Altium.

##### Power supply

The power is supplied to the voltage conditioning board by the [custom voltage distribution board](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript/Custom_voltage_distribution): +5 V, gnd and -5 V.

##### Inputs

- 3.3 V TTL trigger signal
- 3.3 V (>=1 kHz) PWM control signal (to set the power of the laser diode)

##### Output

- Out: the Out signal should be fed directly at the intersection of the two resistors on the modified EU-38-TTL (see [previous section](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript)).
- 3.3 V voltage supply: can be used with a potentiometer to generate a manual control signal (see the [wiring](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript/Wiring) submodule for how we used a switch and a potentiometer for manual power control).



> Note: see [the wiring section](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript/Wiring) for more details on how we wired the custom boards in the electronics box.