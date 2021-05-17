# PCBs

These are the PCB files. All PCBs so far have been manufactured at JLCPCB, so I include the JLCPCB SMT BOM and placement files.

V0.6 is a work in progress. The planned changes for this revision are:
* Fix some minor silkscreen errors
* Implement the improved STM32 reset circuit designed by Gondolindrim, described [here](http://acheronproject.com/reset_article/principle.html) under "Improving over ishtob’s circuit". The reset circuit on past versions can get the microcontroller into the DFU bootloader for flashing, but can't do a hardware reset, which increases the risk of bricking in case a software reset is not possible (due to an interrupted flashing process, corrupted firmware, or other). On the new version, a short press does a simple reset, while a long press allows the microcontroller to enter the DFU bootloder. 
* Implement some EMI best practices, such as minimizing ground plane disruptions underneath the switching converter. I may run Boston through FCC testing at some point, so I would like to  

V0.6D is a planned version of V0.6 which is intended for use with a USB-C daughterboard, such as the [C3 Unified Daughterboard](https://github.com/ai03-2725/Unified-Daughterboard). This removes the USB-C connector and the ESD protection IC (as both of those will be on the daughterboard) and adds a JST connector to connect to the daughterboard.

V0.6J is a planned version of V0.6 where all of the parts (except for the RGBLED and the reset switch, which are both through hole) can be assembled by JLCPCB. This removes backlight LED support and uses a linear regulator for the 5V->3.3V converesion rather than a switching one (the AP63203WU-7 and inductor are replaced with a TLV1117-33 LDO). Due to the reduced amount of available 3.3V current this means I am removing backlight support. Since this can be ordered fully-assembled from JLCPCB, this should make it easier for people to obtain PCBs.

V0.5.2 was what shipped in the Round 0 barebones kit sale, and has been verified to work. JLCPCB at the time was not able to solder on connectors, and was out of stock of STM32F072 microcontrollers, so those parts are not included on the manufacturing files. JLCPCB also did not carry the fuse, the AP63203WU-7 buck controller, or the , so those parts are not included in the manufacturing files for JLCPCB SMT, and were soldered on by hand. 

Older PCB files are not included but can be accessed through the Git history.

## Older PCB Changelog

* V0.5.2 - October 6, 2020 - Removed a loop in the ground plane (which did not seem to affect functionality), and made some minor changes to the silkscreen. Increased thermal clearances around the RGBLED to make it easier to solder. Minor silkscreen fixes. Tested and working. People who bought Round 0 barebones kits received this PCB.

* V0.5.1 - September 23, 2020 - this fixed the routing errors in V0.5, and slightly improved the silkscreen graogucs. The grounding screw hole is now connected to ground via a ferrite bead. Tested and working. Beta testers received fixed V0.5 and V0.5.1 boards.

* V0.5 - September 16, 2020 - added split space and WKL support, a grounding pad for the metal case, changed silkscreen somewhat, and changed the microcontroller footprint to be able to take both LQFP-48 and UFQFPN48 due to shortages of LQFP48 STM32F072's. This had several routing errors and requires some fixes for all features to work.

* V0.4 - August 11, 2020 - a complete redesign. Placed everything on a single PCB, with a centered USB-C port. The F-key clusters are moved closer to the main alpha keys. Switched to SMD diodes. Designed for both a 3D-printed/FR4 case, and a CNC metal case. Working. 

* V0.3 and earlier - these used a two-PCB design, with microcontroller, USB port, and associated components on the daughterboard, and a completely through-hole main PCB. Not compatible with the published case designs. The firmware is largely similar, though the matrix is different.

