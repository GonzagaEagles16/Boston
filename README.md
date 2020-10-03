# [NotYetAcheron] 121-S-THT-MX-TH-WI (Codename "Boston")

![1st prototype](https://github.com/bluepylons/Boston/raw/master/graphics/prototype_1_pic.JPG)
![3D-printed/FR4 version](https://github.com/bluepylons/Boston/raw/master/graphics/3D-printed-prototype.JPG)

## Introduction 
Boston is a compact 120% with a full-complement of 18 programmable keys, in a footprint 2u narrower than a full-size, and only about 1.5u wider than a 96%. 

The immediate inspiration for Boston was the DriftMechanics [Austin](https://github.com/Gondolindrim/Austin), as well as the [7-row Thinkpad keyboards](http://www.notebookreview.com/picture/?f=60846) found on Thinkpads of the T420 generation and older. The general idea was to make a narrower full-size that retained both the 2u numpad "0" and traditional 2x3 Ins/Del/Home/End/PgUp/PgDn nav block, by expanding vertically. 

The name is a pun off Austin, since the layout is derived from it. I also grew up in Boston. 

## Status

This is a work in progress. 

The current version (V0.5.1, in the "Boston - Current design" folder) is currently being prototyped. A list of errata will be produced once it has been fully tested. I intend to run a GB for this keyboard in the near future. An older version of the PCB (V0.4) is fully working. 

STL files for the 3D-printed case are available under the "3D-printed case - parts" folder. Full STEPs, Fusion, and a bill-of-materials will be released after the group buy runs.

The aluminum version is still being prototyped. Case files for those will likely be released after a couple group buy runs.

An older version (V0.3) used a two-PCB design with the controller on a daughterboard, and a different matrix. Only two of these were produced. 

The Interest Check thread is [here](https://geekhack.org/index.php?topic=106501.0) on Geekhack.

## Supported layouts

![Boston layouts](https://github.com/bluepylons/Boston/raw/master/graphics/bostonKLE.png)

Click [this link](http://www.keyboard-layout-editor.com/#/gists/75e63e00e1acc52cdb8eeda7f8ac4ba6) for the KLE file for Boston.

Note - The 1u Numpad + and - switches, in substitution of the normal 2u + key, are west-facing, which may not be compatible with some keycaps.

## PCB Renders 

Renders done with [tracespace.io](https://tracespace.io/).
![Keyboard top](https://github.com/bluepylons/Boston/raw/master/graphics/PCB-top-V0.5.1.png)
![Keyboard bottom](https://github.com/bluepylons/Boston/raw/master/graphics/PCB-bottom-V0.5.1.png)

## Features:
* 121-key in standard ANSI configuration
* Alps EC11E rotary encoder above the Escape key 
* Full-size numpad with 2u "0" key
* Traditional 2x3 Ins/Del/Home/End/PgUp/PgDn navblock 
* Uses keys found in GMK base kits (except for programmable keys)
* RGBLED layer-status indicator light
* ISO enter key, split backspace, split numpad 0, and WKL bottom row support 
* Optional 3mm through-hole LED backlight (dimmable as a single block only)
* USB-C
* STM32F072 controller running QMK. Circuitry is derived from the Austin. 

## Copyright Notice

The PCB files and hardware designs are released under the [Acheron Open-Hardware License V1.2](http://acheronproject.com/license/license.html). 

All files in "QMK files (temporary home)", like all other QMK firmware, are released under the [GNU Public License, Version 2](https://github.com/qmk/qmk_firmware/blob/master/LICENSE). 

The map artwork in Single PCB design/3D printed case- FR4 part files/Bottom was created using OpenStreetMap data, © OpenStreetMap contributors, under OpenStreetMap's [conditions](https://www.openstreetmap.org/copyright). 

## Libraries

The KiCAD files are done using the nightly builds, as the Acheron Library is currently on the nightlies and aren't compatible with the 5.1.6 stable build. This will be updated over to the next stable KiCAD release whenever that comes out (which will  be the release is after 5.1.6) This project uses the [Acheron Library](https://github.com/AcheronProject/AcheronLibrary).

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


