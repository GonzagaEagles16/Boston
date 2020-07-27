# [NotYetAcheron] 121-S-THT-MX-TH-WI (Codename "Boston")

![1st prototype](https://github.com/bluepylons/Boston/raw/master/graphics/prototype_1_pic.JPG)

## Introduction 
Boston is a compact 120% with a full-complement of 18 programmable keys, in a footprint 2u narrower than a full-size, and only about 1.25u wider than a 96%. 

The immediate inspiration for Boston was the DriftMechanics [Austin](https://github.com/Gondolindrim/Austin), as well as the [7-row Thinkpad keyboards](http://www.notebookreview.com/picture/?f=60846) found on Thinkpads of the T420 generation and older. The general idea was to make a narrower full-size that retained both the 2u numpad "0" and traditional 2x3 Ins/Del/Home/End/PgUp/PgDn nav block, by expanding vertically. 

The Geekhack build thread on this keyboard [here](https://geekhack.org/index.php?topic=106239.0).

The name is a pun off Austin, since the layout is derived from it.

## Status

This is a work in progress. The current PCB files (as of July 6, 2020) have been sent out to JLCPCB for fab and will be prototyped shortly. The firmware still needs some work.

Case files will be released after one or more rounds of group buys have been run. This is unfortunately necessary to prevent third party group buys from running parallel to the main group buy for the time being. 

The Interest Check thread is [here](https://geekhack.org/index.php?topic=106501.0) on Geekhack.

## Supported layouts

![Boston layouts](https://github.com/bluepylons/Boston/raw/master/graphics/bostonKLE.png)

Click [this link](http://www.keyboard-layout-editor.com/#/gists/75e63e00e1acc52cdb8eeda7f8ac4ba6) for the KLE file for Boston.

Note - The 1u Numpad + and - switches, in substitution of the normal 2u + key, are west-facing, which may not be compatible with some keycaps.

## Renders

Renders done with [tracespace.io](https://tracespace.io/).
![Keyboard top](https://github.com/bluepylons/Boston/raw/master/graphics/keyboard-top-V0.3.png)
![Keyboard bottom](https://github.com/bluepylons/Boston/raw/master/graphics/keyboard-bottom-V0.3.png)
![Controller top](https://github.com/bluepylons/Boston/raw/master/graphics/controller-top-V0.3.png)
![Controller bottom](https://github.com/bluepylons/Boston/raw/master/graphics/controller-bottom-V0.3.png)

## Features:
* 121-key in standard ANSI configuration
* Full-size numpad with 2u "0" key
* Traditional 2x3 Ins/Del/Home/End/PgUp/PgDn navblock 
* Uses keys found in GMK base kits (except for programmable keys)
* RGBLED layer-status indicator light
* ISO enter key support 
* Optional 3mm through-hole LED backlight (dimmable as a single block only)
* USB-C
* STM32F072 controller on a daughterboard that nests under the F5-F8 keys. Circuitry is derived from the Austin. 
* The base keyboard without backlighting is all-throughole. Current-limiting resistors for the backlight LEDs are 0805 SMD though. All other SMD components are on the controller daughterboard. 
* Optional Alps EC11E rotary encoder above the Escape key 

## Copyright Notice

The PCB files and hardware designs are released under the [Acheron Open-Hardware License V1.2](http://acheronproject.com/license/license.html). 

All files in "QMK files (temporary home)" under the "BostonV0 - two PCB design", like all other QMK firmware, are released under the [GNU Public License, Version 2](https://github.com/qmk/qmk_firmware/blob/master/LICENSE). 

## Libraries

The KiCAD files are done using the nightly builds, as the Acheron Library is currently on the nightlies and aren't compatible with the 5.1.6 stable build. This will be updated over to the next stable KiCAD release whenever that comes out (which will  be the release is after 5.1.6) This project uses the [Acheron Library](https://github.com/AcheronProject/AcheronLibrary).

 The KiCAD files use projet-specific paths to the Acheron Library. To set this up - in KiCAD, open Preferences > Configure Paths. Add a new entry, with ACHERONLIB for the name, and for the path, the directory where the AcheronLibrary folder resides in.

## Errata 

### Keyboard PCB Rev 0.2 errata
* The diode for the numpad enter-key hits the stabilizer wire, and has to be soldered onto the underside.
* Some silk-screen overlaps with pads
* Forgot the "Acheron Library"  text after the "Powered by" text

### Controller PCB Rev 0.2 errata
* The FB pin for the AP63203WU-7 buck controller was mistakenly routed to ground. **This will cause 5V to appear at the output and kill the controller**. 
* The ARM SWD header uses a 1x10 header instead of a 2x5 header. 

## Acknowledgements

Many thanks to:
* The [Acheron Project](http://acheronproject.com/) - the KiCAD library and the source files for the Austin have been invaluable for designing this board.
* The designers of the Austin (Driftingbunnies, PheonixStarr and Gondolindrim)
* Gondolindrim, for assistance and feedback with the PCB design, as for running the Acheron project
* KiCAD, for being an awesome free open-source PCB design tool
* [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/), where I designed the layout. 
* [Swill's plate generator](http://builder.swillkb.com/), which I used for making the plate.



