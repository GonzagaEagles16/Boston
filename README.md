![PCB version](https://img.shields.io/badge/PCB%20Version-pre%20Alpha-green.svg?style=flat) ![Prototype version](https://img.shields.io/badge/Prototype%20Version-pre%20Alpha-green.svg?style=flat) ![Firmware](https://img.shields.io/badge/Firmware-Passing-green.svg?style=flat)


# [NotYetAcheron] 121-S-SM-MX-STM32-TH-WI (Codename "Boston")

![1st prototype](https://github.com/bluepylons/Boston/raw/master/graphics/prototype_1_pic.JPG)
![3D-printed/FR4 version](https://github.com/bluepylons/Boston/raw/master/graphics/3D-printed-prototype.JPG)

## Introduction 
Boston is a compact 120% with a full-complement of 18 programmable keys, in a footprint 2u narrower than a full-size, and only about 1.5u wider than a 96%. Both a 3D-printed/FR4 case and a CNC aluminum case will be available.

The immediate inspiration for Boston was the DriftMechanics [Austin](https://github.com/Gondolindrim/Austin), as well as the [7-row Thinkpad keyboards](http://www.notebookreview.com/picture/?f=60846) found on Thinkpads of the T420 generation and older. The general idea was to make a narrower full-size that retained both the 2u numpad "0" and traditional 2x3 Ins/Del/Home/End/PgUp/PgDn nav block, by expanding vertically. 

The name is a pun off Austin, since the layout is derived from it. I also grew up in Boston. 

## Supported layouts

![Boston layouts](https://github.com/bluepylons/Boston/raw/master/graphics/bostonKLE.png)

Click [this link](http://www.keyboard-layout-editor.com/#/gists/75e63e00e1acc52cdb8eeda7f8ac4ba6) for the KLE file for Boston.

## Features:
* 121-key in standard ANSI configuration
* Alps EC11E rotary encoder above the Escape key 
* Full-size numpad with 2u "0" key
* Traditional 2x3 Ins/Del/Home/End/PgUp/PgDn navblock 
* Uses keys found in GMK base kits (except for programmable keys)
* RGBLED layer-status indicator light (layer-status indication not yet implemented)
* ISO enter key, split backspace, split numpad 0, split space, and WKL bottom row support 
* Optional through-hole LED backlight (dimmable as a single block only)
* USB-C
* STM32F072 controller running QMK. Circuitry is derived from the Austin. 

## Status

This is a work in progress.  The Geekhack Interest Check thread is [here](https://geekhack.org/index.php?topic=106501.0) on Geekhack. Updates will occasionally be posted there.

The current version (V0.5.2, in the "Boston - Current design" folder) has been prototyped and is working. 

STL files for the 3D-printed/FR4 case are available under the "3D-printed case - parts" folder. Full STEPs, Fusion, and a bill-of-materials will be released after the group buy runs.

The aluminum version is still being prototyped. Unfortuantely, due to my likely arrangements with my vendor for this version, the case files for the aluminum version are unlikely to be open-sourced in the near future.

There is a working version of QMK, though RGB layer status indication has not yet been implemented (though there is basic RGB functionality imlemented).

I may implement VIA in the future as the microcontroller supports it, but it's not currently in the cards. 

## PCB Renders 

Renders done with [tracespace.io](https://tracespace.io/).
![Keyboard top](https://github.com/bluepylons/Boston/raw/master/graphics/PCB-top-V0.5.2.png)
![Keyboard bottom](https://github.com/bluepylons/Boston/raw/master/graphics/PCB-bottom-V0.5.2.png)

## PCB Changelog

* V0.3 and earlier - these used a two-PCB design, with microcontroller, USB port, and associated components on the daughterboard, and a completely through-hole main PCB. Not compatible with the published case designs. The firmware is largely similar, though the matrix is different.
* V0.4 - August 11, 2020 - a complete redesign. Placed everything on a single PCB, with a centered USB-C port. The F-key clusters are moved closer to the main alpha keys. Switched to SMD diodes. Designed for both a 3D-printed/FR4 case, and a CNC metal case. Working. 
* V0.5 - September 16, 2020 - added split space and WKL support, a grounding pad for the metal case, changed silkscreen somewhat, and changed the microcontroller footprint to be able to take both LQFP-48 and UFQFPN48 due to shortages of LQFP48 STM32F072's. This had several routing errors and requires some fixes for all features to work.
* V0.5.1 - September 23, 2020 - this fixed some routing errors in V0.5, and slightly improved the silkscreen. The grounding pad is now connected to ground via a ferrite bead. Tested and working.
* V0.5.2 - Removed a big loop in the ground plane (which did not seem to affect functionality), and made some minor changes to the silkscreen. Increased thermal clearances around the RGBLED to make it easier to solder. Minor silkscreen fixes. Tested and working.

## Copyright Notice

The PCB files and hardware designs are released under the [Acheron Open-Hardware License V1.2](http://acheronproject.com/license/license.html). 

All files in "QMK files (temporary home)", as required by QMK and ChibiOS's license, are released under the [GNU Public License, Version 3](https://www.gnu.org/licenses/gpl-3.0.en.html). 

The map artwork in Single PCB design/3D printed case- FR4 part files/Bottom was created using OpenStreetMap data, © OpenStreetMap contributors, under OpenStreetMap's [conditions](https://www.openstreetmap.org/copyright). The resulting KiCAD footprint and PCB files for the bottom FR4 panel containing the artwork is specifically released under the [Open Data Commons Open Database License](https://opendatacommons.org/licenses/odbl/) 

## Libraries

The KiCAD files are done using the 5.99nightly builds, as the Acheron Library is currently on the nightlies and aren't compatible with the 5.1.6 stable build. This will be updated over to KiCAD V6 whenever that is released This project uses the [Acheron Library](https://github.com/AcheronProject/AcheronLibrary).

 The KiCAD files use project-specific paths to the Acheron Library. To set this up - in KiCAD, open Preferences > Configure Paths. Add a new entry, with ACHERONLIB for the name, and for the path, the directory where the AcheronLibrary folder resides in.

## Acknowledgements

Many thanks to:
* The [Acheron Project](http://acheronproject.com/) - the KiCAD library and the source files for the Austin have been invaluable for designing this board.
* The designers of the Austin (Driftingbunnies, PheonixStarr and Gondolindrim). The layout, schematics, and firmware were derived from that board.
* Gondolindrim, for assistance and feedback with the PCB design, as for running the Acheron project.
* KiCAD, for being an awesome free open-source PCB design tool.
* [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/), where I designed the layout. 
* [Swill's plate generator](http://builder.swillkb.com/) and [Ai03's plate generator](https://kbplate.ai03.com/), which I used for making the plate.
* [Maperitive](http://maperitive.net/) and [OpenStreetMap](https://www.openstreetmap.org/#map=4/38.01/-95.84), which was used to generate the map artwork on the bottom of the 3D-printed/FR4 case. 


