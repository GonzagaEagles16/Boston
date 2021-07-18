## Vial firmware

These are the files for [Vial](https://get.vial.today/), an open-source alternative to VIA that allows you to reprogram your keymap on-the-fly. 

*Note that Vial is currently in beta, and there may be bugs. Use at your own risk. The Vial firmware for Boston has also only been tested on the standard layout, and although alt layouts (ISO, WKL, etc.) are supported they have not been tested and may have issues. Please contact me if there are any issues.* 

If you just want to use Vial, flash the boston_vial.bin file (using QMK Toolbox, dfu-util, or another utility). Vial should recognize the keyboard, and let you remap keys.

The files in the \boston folder are used to compile the base firmware in vial-QMK. These may not compile in regular QMK due to differences between vial-QMK and regular QMK. These files are kept here as I doubt the QMK master repository will accept these.

Current files use Vial Version 0.4

All files in this directory are licensed under the GNU General Public License V3.0.
