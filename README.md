# Game-Boy-MGB-Heavy
A Game Boy Pocket transplanted into a DMG Game Boy form factor

## Summary
The Game Boy Pocket (MGB-001) form factor, while aesthetically pleasing has a number of issues with its design: AAA batteries, hand-cramping size, small buttons, and lack of overally weight and heft.

This project attempts to allieviate some of these concerns by re-creating a DMG-CPU board using a mix of transplanted and off-the-shelf components, but with the MGB CPU.

It is in the broadest sense a fork of [Kamicane's Super DMG](https://github.com/kamicane/Super-DMG-01) (and borrows very heavily from that design)
The MGB CPU has the same footprint as a DMG CPU except the pinouts are in different locations and it has onboard VRAM. 

I've rerouted the board for MGB pinout, removed the VRAM IC and replaced the bulk of the schematic and component footprints with the equivalent donor part from the MGB where available.

<img src="https://github.com/ConsolesandCasks/CPU-MGB-Heavy/blob/main/MGB_Heavy_1_front_blank.png" width=400 height=400>  <img src="https://github.com/ConsolesandCasks/CPU-MGB-Heavy/blob/main/MGB_Heavy_1_back.png" width=400 height=400>

## Notes
Most of the SMD components that are available on the MGB are re-utilized, but I'll provide a BOM to list them anyway.

I have also removed the USB port and wires/connectors associated with Lipo usage. Future revisions may re-implement this in some form. Rev 1.1 adds an optional OEM style DC jack using new parts.

Current repository contains this readme, forked materials, schematic and gerbers, KiCad project files and a full BOM reference for rev 1.1.

Gerber files for the latest revision are included in *MGB_Heavy_JLC_r1_1.zip*

## Credits
[Kamicane](https://github.com/kamicane/) for the [Super DMG](https://github.com/kamicane/Super-DMG-01) project that serves as a base for this project

[Gekkio](https://github.com/Gekkio/) for [MGB](https://github.com/Gekkio/gb-schematics/tree/main/MGB-xCPU) and [DMG](https://github.com/Gekkio/gb-schematics/tree/main/DMG-CPU-06) schematics, as well as a number of symbols and footprints from [Gekkio KiCad libs](https://github.com/Gekkio/gekkio-kicad-libs)

[Bucket Mouse](https://github.com/MouseBiteLabs/) for the [DMGC](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color) project that got me down this rabbit hole and some more references to help with footprints and fit as well as compatible power and headphone boards

[ViS](https://github.com/vISmodding/) for another [DMG replacement PCB](https://github.com/VISmodding/VIS_Game_Boy_DMG) project that I referenced and utilized some replacement components from, footprints, and fit as well as (hopefully) compatible headphone boards

[N64-Freak](https://github.com/N64-Freak) for a [replacement MGB board](https://github.com/N64-Freak/GB-Mods/tree/main/Pocket) and [Skimzor](https://github.com/skimzor) for another [replacement MGB board BOM](https://skimzor.github.io/MGB-IBOM/) for BOM reference

[Natalie the Nerd](https://github.com/nataliethenerd) for the basis of the X1 footprint from her [AGB project](https://github.com/nataliethenerd/AGB-CPU-03)

DC jack idea from [this video by Joe Ostrander](https://www.youtube.com/watch?v=d2NDXVqlKTY) of yet another DMG replacement PCB

## Bill of Materials (BOM)
The complete BOM for the board itself is included in the excel spreadsheet including replacement passive component numbers for anything that you are unable to transplant. All DMG parts can be harvested from a broken DMG instead as long as the part itself is in working condition, but I'd advise using an alternative.

To give a high-level breakdown for the remainder, this is what you'll need:
* **Original Game Boy Pocket** console or motherboard
  * Everything* required for this build comes from above the cartridge slot. Great news if you're using the bottom half for a CHOP method Pocket Color  <sub>*C31 and C32 can be reused but it is inadvised. I have replaced these with new Tantalum capacitors in the BOM per Kamicane's original design</sub>
* **DMG compatible shell** as well as **buttons** and **membranes** (or suitable alternatives)
  * IPS kits should use a shell designed for the IPS kit - OEM front boards can use OEM shells
* **Screen Kit** - one of the following:
  * Funnyplaying DMG IPS Screen Kit (w/ front board) (tested)
  * OEM DMG Front board (tested compatible as long as the VEE line is intact) - *this requires an original DMG power supply board* and will not work with alternate boards that do not carry VEE
  * Other IPS kits may work too as long as they have a front board but are currently untested
* **Audio Board** - one of the following:
  * [Kamicane's Super DMG Jack](https://github.com/kamicane/Super-DMG-01/tree/main/super-dmg-jack) (tested in both configurations)
  * [ViS Modding DMG Audio Board](https://github.com/VISmodding/VIS_Game_Boy_DMG/) (untested)
  * [Bucket Mouse DMGC-HDP](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color/tree/main/DMGC-HDP-01) requires original DMG headphone jack (untested)
  * OEM DMG Headphone Board (tested)
* **Power Board** - one of the following:
  * [Bucket Mouse DMGC-PWR](https://github.com/MouseBiteLabs/Game-Boy-DMG-Color/tree/main/DMGC-PWR-01) - NOT COMPATIBLE WITH OEM SCREENS (tested)
  * OEM DMG Power Board (tested)
  * Other replacement power boards might be compatible, but I have not tested them, use at your own risk
    * PLEASE NOTE: I will not help you troubleshoot other people's headphone and power board designs, bug them if you have issues 
* [Replacement Power Switch](https://www.lcsc.com/product-detail/Slide-Switches_HOOYA-SK-24D02G3_C2939338.html) (or OEM  harvested/NOS DMG power switch)
* [DMG Cartridge Slot](https://www.aliexpress.us/item/3256802533298738.html)
* DMG Link Port (harvested from 4 player adapter DMG-007 or OEM DMG)
* [DMG Volume Knob](https://www.aliexpress.us/item/3256804088642332.html)
* [DMG Battery Contacts](https://www.aliexpress.us/item/3256801650618764.html)
* [DMG FPC Connector](https://www.aliexpress.us/item/3256804638192354.html)
* DMG Speaker (note, with the ViS audio board or Kamicane's Super DMG Jack Amp you may need a different speaker as referenced in those repositories)
* [Replacement DC jack (DC-002)](https://www.lcsc.com/product-detail/AC-DC-Power-Connectors_XKB-Connectivity-DC-002-2-0A-1-3_C381119.html) (can be disabled via solder jumper) - there is an additional fuse and diode I've added for use with this as well - they may not be necessary but are in the BOM as a precaution. There are multiple versions of this jack - make sure you get one that has a 1.3mm inner diameter and at least 1.0A max current rating.
* 
## Extras
*sdmg_1.8jb_gerbers.zip* is a standard Super DMG CPU 1.8 board with the switch, DC jack, and some of the pad changes noted above but still routed to utilize the DMG or Super Game Boy CPU.
These files also fix the Link Port routing that is reversed on the release version Super DMG 1.8 and earlier.

## License
This work is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License.](http://creativecommons.org/licenses/by-sa/4.0/)

## Changelog

### Rev 1.1

Added DC jack, jumper, and supporting components; removed some unused pads; re-introduced Kamicane's "usb lip" for the DC jack

### Rev 1.0

Initial design
