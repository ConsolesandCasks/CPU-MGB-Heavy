# Game-Boy-MGB-Heavy
A Game Boy Pocket transplanted into a DMG Game Boy form factor

## Summary
The Game Boy Pocket (MGB-001) form factor, while aesthetically pleasing has a number of issues with its design: AAA batteries, hand-cramping size, small buttons, and lack of overally weight and heft.
This project attempts to allieviate some of these concerns by re-creating a DMG-CPU board using a mix of transplanted and off-the-shelf components, but with the MGB CPU.
It is in the broadest sense a fork of [Kamicane's Super DMG](https://github.com/kamicane/Super-DMG-01) (and borrows very heavily from that design)

<img src="https://github.com/ConsolesandCasks/CPU-MGB-Heavy/blob/main/MGB_Heavy_1_front.png" width=400 height=400>  <img src="https://github.com/ConsolesandCasks/CPU-MGB-Heavy/blob/main/MGB_Heavy_1_back.png" width=400 height=400>

## Notes
Most of the SMD components that are available on the MGB I've replaced, compared to the original Super DMG project, to match the MGB schematic.
I have also (possibly temporarily) removed the USB port and wires/connectors associated with Lipo usage until I've done some testing of my own.
This project is UNTESTED as of this version of the readme (Aug 14 2023) - current repository contains this readme, and forked materials only. KiCad project files and Gerbers will be added once I've tested the initial design.

## Credits
[Kamicane](https://github.com/kamicane/) for the [Super DMG](https://github.com/kamicane/Super-DMG-01) project that serves as a base for this project

[Gekkio](https://github.com/Gekkio/) for [MGB](https://github.com/Gekkio/gb-schematics/tree/main/MGB-xCPU) and [DMG](https://github.com/Gekkio/gb-schematics/tree/main/DMG-CPU-06) schematics, as well as a number of symbols and footprints from [Gekkio KiCad libs](https://github.com/Gekkio/gekkio-kicad-libs)

[Bucket Mouse](https://github.com/MouseBiteLabs/) for the [DMGC](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color) project that got me down this rabbit hole and some more references to help with footprints and fit as well as compatible power and headphone boards

[ViS](https://github.com/vISmodding/) for another [DMG replacement PCB](https://github.com/VISmodding/VIS_Game_Boy_DMG) project that I referenced and utilized some replacement components from, footprints, and fit as well as compatible headphone boards

[N64-Freak](https://github.com/N64-Freak) for a [replacement MGB board](https://github.com/N64-Freak/GB-Mods/tree/main/Pocket) so I could reference its BOM 

[Natalie the Nerd](https://github.com/nataliethenerd) for the X1 footprint from her [AGB project](https://github.com/nataliethenerd/AGB-CPU-03)

If I do implement a DC jack, it will likely be the one used in [this video by Joe Ostrander](https://www.youtube.com/watch?v=d2NDXVqlKTY) of yet another DMG replacement PCB

## Bill of Materials (BOM)
The complete BOM will be included in an excel spreadsheet once I have tested the board (including replacement passive component numbers for missing transplant items). All DMG parts can be harvested from a broken DMG instead as long as the part itself is in working condition

To give a high-level breakdown, this is what you'll need:
* Original Game Boy Pocket console or motherboard
  * Everything* required for this build comes from above the cartridge slot. Great news if you're using the bottom half for a CHOP method Pocket Color  <sub>*C32 and C33 can be reused but it is inadvised. I have replaced these with new Tantalum capacitors in the BOM per Kamicane's original design</sub>
* Funnyplaying DMG IPS shell as well as buttons and membranes or suitable alternatives
* Funnyplaying DMG IPS Screen Kit (w/ front board)
  * Other IPS kits may work too as long as they have a front board, and I've left the VEE wire for an original front board, but I have not tested this and take no responsibility for any damage or issues using this would cause.
* Audio Board - one of the following:
  * [Kamicane's Super DMG Jack](https://github.com/kamicane/Super-DMG-01/tree/main/super-dmg-jack)
  * [ViS Modding DMG Audio Board](https://github.com/VISmodding/VIS_Game_Boy_DMG/)
  * [Bucket Mouse DMGC-HDP](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color/tree/main/DMGC-HDP-01) requires original DMG headphone jack
  * Original DMG Headphone Board
* Power Board - one of the following:
  * [Bucket Mouse DMGC-PWR](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color/tree/main/DMGC-PWR-01) - NOT COMPATIBLE WITH OEM SCREENS
  * Original DMG Power Board
  * Other replacement power boards might be compatible, but I have not tested them, use at your own risk
    * PLEASE NOTE: I will not help you troubleshoot other people's headphone and power board designs, bug them if you have issues 
* [Replacement Power Switch](https://www.lcsc.com/product-detail/Slide-Switches_HOOYA-SK-24D02G3_C2939338.html) (or original harvested/NOS DMG power switch)
* [DMG Cartridge Slot](https://www.aliexpress.us/item/3256802533298738.html)
* DMG Link Port (harvested from 4 player adapter DMG-007 or original DMG)
* [DMG Volume Knob](https://www.aliexpress.us/item/3256804088642332.html)
* [DMG Battery Contacts](https://www.aliexpress.us/item/3256801650618764.html)
* DMG Speaker (note, with the ViS audio board you may need a different speaker as referenced in his repository)

## License
This work is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License.](http://creativecommons.org/licenses/by-sa/4.0/)
