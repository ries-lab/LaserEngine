## Voltage distribution board

The voltage distribution board simplifies the wiring within our electronics box and allows delivering negative voltage to the signal conditioning board without having a negative power supply.

#### Parts

Note that we worked with two power supplies:

- [Power supply #1](https://www.reichelt.com/de/en/eco-friendly-plug-in-power-supply-max-1000-ma-usb-mw-3k10gs-p87339.html?&trstct=pos_0) (set to 6 V, 1 A)

- [Power supply #2](https://www.reichelt.com/de/de/steckernetzteil-12-w-5-v-2-4-a-stabilisiert-gs15e-1p1j-p161604.html?&trstct=pos_0) (5 V, 2.5 A)

  

#### Guidelines

In order to supply voltage to the laser diode driver and to the signal conditioning board:

1. Wire the power supplies ground to the ground on the voltage distribution board.

2. Set power supply #1 voltage to 6 V. Wire its positive pin to the +6 V area of the board.

3. Wire power supply #2 positive pin to the +5 V area of the board.

   > Note: We actually soldered an interrupter between the power supplies positive pin and the voltage distribution board to be able to turn off the circuit. See the [wiring section](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript/Wiring) for more details.

4. The voltage conditioning boards have 3 pins for the voltage supply: -5 V, GND and +5 V. Wire them accordingly using pins from the -5 V, ground and +5 V areas on the voltage distribution board.

5. The laser diode driver require different voltage, depending on the diodes they power. Wire the ground to the ground area, then the positive signal from the following voltage area on the board:

   | 405 nm & 488 nm | 638 nm (x2) |
   | :-------------: | :---------: |
   |      +5 V       |    +6 V     |

   

> Note: see [the wiring section](https://github.com/ries-lab/LaserEngine/tree/master/Electronics/Electronics_manuscript/Wiring) for more details on how we wired the custom boards in the electronics box.

