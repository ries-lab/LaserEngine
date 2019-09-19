## Electronics

To control the laser diodes, we imposed a set of constraints:

- Computer control of the **laser power** using a **[PWM](https://www.arduino.cc/en/tutorial/PWM) signal** ([Mojo FPGA](https://github.com/jdeschamps/MicroMojo) or Arduino).

- **Triggering of the laser diodes** (μs range) using a **TTL signal**.

- **Capping of the current** supplied to the laser diodes to avoid damages.


We present here two systems to drive the diodes: the electronics used in the manuscript and an alternative solution. Both are based on custom boards and commercial laser diode driver.

#### Current and voltage requirements

Note that different laser diodes have different voltage and current requirements, which complicates the task of finding a unique solution for all diodes of the laser engine:

| From the datasheets   | 405 nm, 80 mW <br />(dl-7146-301s, Sanyo) | 488 nm, 55 mW <br />(BLD-488-55, lasertack) | 640 nm, 700 mW <br />(HL63193MG, Oclaro) |
| --------------------- | ----------------------------------------- | ------------------------------------------- | ---------------------------------------- |
| Threshold current     | 60 mA                                     | 60 mA                                       | 250 mA                                   |
| Max operating current | 140 mA                                    | 135 mA                                      | 1000 mA                                  |
| Max operating voltage | 6 V                                       | 7.5 V                                       | 2.6 V                                    |

#### Solutions

We explored two solutions to control the laser diodes (we highlighted in bold each feature that is more advantageous in one version than in the other):

|                      |      [Electronics (manuscript)](Electronics_manuscript)      |     [Electronics (alternative)](Electronics_alternative)     |
| -------------------- | :----------------------------------------------------------: | :----------------------------------------------------------: |
| Status               |               **Daily use on our microscopes**               |                   Tested with a prototype                    |
| Inputs voltage       |                     3.3 V (PWM and TTL)                      |                **3.3 V or 5 V (PWM and TTL)**                |
| LD driver            | **4 x [EU-38-TTL](http://www.roithner-laser.com/ld_electronics.html) (total ~80 euros)** | 2 x [LD3000R](https://www.thorlabs.de/thorproduct.cfm?partnumber=LD3000R) + 2 x [LD1255R](https://www.thorlabs.de/thorproduct.cfm?partnumber=LD1255R) (total >600 euros) |
| Modified LD driver   |                             Yes                              |                            **No**                            |
| Power supplies       | **1 x [5 V (2.5 A)](https://www.reichelt.com/de/de/steckernetzteil-12-w-5-v-2-4-a-stabilisiert-gs15e-1p1j-p161604.html?&trstct=pos_0) + 1 x [6 V (1 A)](https://www.reichelt.com/de/en/eco-friendly-plug-in-power-supply-max-1000-ma-usb-mw-3k10gs-p87339.html?&trstct=pos_0)** | [See LD1255R power supply](https://www.thorlabs.de/newgrouppage9.cfm?objectgroup_id=1366) and <br />contact Thorlabs for the LD3000R |
| Power supplies price |                        ~ **24 euros**                        |                      prob. ~ 300 euros                       |
| Custom boards        | 4 x [signal conditioning](Custom_signal_conditioning) + 1 x [voltage distribution](Custom_voltage_distribution) |         **1 x [signal conditioning](Custom_board)**          |
| LD pulsing           |                           ~ **μs**                           |                             ~ ms                             |

#### Notes:

- **Important**: The alternative electronics has only been tested **with a prototype**, while the manuscript version is used daily in our microscopes.
- In both cases, we generated the TTL and PWM signals using a Mojo FPGA. The FPGA firmware was based on the [MicroMojo project](https://github.com/jdeschamps/MicroMojo) and interfaced with the computer using [Micro-manager](https://micro-manager.org/). Alternatively, an Arduino can be used (also compatible with Micro-Manager).
- Each custom board was designed in [Altium](https://www.altium.com/); we uploaded here the Altium projects. Altium projects can be opened with a free license of the [Altium Designer Viewer](https://www.altium.com/altium-designer-viewer).
- The bill of materials for each custom board was exported in a format compatible with [Beta Layout](https://uk.beta-layout.com/pcb/) requirements. These can be used with the circuit PCB layout to order an already assembled board.



Both versions were designed by **Christian Kieser, Electronics workshop, EMBL**.