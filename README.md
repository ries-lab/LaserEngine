# ![Logo](logo.png) Open-source laser engine



![Laser engine](laserengine.jpg)

Blueprints for a low-cost laser engine compatible with wide-field and localization microscopy. The laser engine is based on affordable, albeit powerful, laser diodes, a square multimode fiber and a speckle-reduction module.


### :information_source: ​How to navigate the repository

The repository contains the following complementary modules:

- [Agitation module](Agitation_Module): a box holding a motor suspended by elastic cords for speckle and noise reduction.
- [Laser diode electronics](Electronics): Electronics to control the power and triggering of the laser diodes from the computer.
- [Laser engine](Laser_Engine): plans and guidelines of the optical path. It contains several submodules:
  - [Laser diodes mount](Laser_Engine/Diodes_Mount): A machined mount to host the TO56-canned laser diodes.
  - [Enclosure](Laser_Engine/Enclosure): A simple box to protect the laser engine from dust and the users from laser light.
  - [**(Optional)** Speckle-reduction for a 561 nm laser](Laser_Engine/LSR): In case of further speckle-reduction needed for a dpss laser, we present an optional element to place in the beam path.



### Repository updates

This repository is updated with the newest developments. If you wish to consult the repository in the state of the publication, please check out the tag **boe** within your local git copy:

```bash
git checkout boe
```

Or download the release [on Github](https://github.com/ries-lab/LaserEngine/releases/tag/boe) or [Zenodo](https://zenodo.org/badge/latestdoi/172924170).



###  :warning: Safety warnings :warning:

- Always work with adequate laser light protection.
- The foam board used in the [enclosure](Laser_Engine/Enclosure) is a fire hazard when subjected to strong laser light. Make sure to place beam stops behind the dichroic mirrors and the polarization beam splitter so that no laser beam hits the foam board panels. 
- Building the [electronics](Electronics) oneself requires experience in soldering and electronics in general. Make sure you are working safely.

#### Cite us

Daniel Schröder\*, Joran Deschamps\*, Anindita Dasgupta, Ulf Matti, and Jonas Ries, "Cost-efficient open source laser engine for microscopy," Biomed. Opt. Express 11, 609-623 (2020), [doi: 10.1364/BOE.380815](https://doi.org/10.1364/BOE.380815)

Repository on Zenodo:
[![DOI](https://zenodo.org/badge/172924170.svg)](https://zenodo.org/badge/latestdoi/172924170)


#### Contact

If you have any question, get in touch with the [Ries group.](https://rieslab.de/#contact)

#### License 

[GNU LGPL](license.txt)


#### Acknowledgements

The electronics was designed by Christian Kieser, Electronics workshop, EMBL.

Pictures credit: *EMBL/Marietta Schupp*
