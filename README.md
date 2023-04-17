# sample_klipper_configs
 Some of the klipper setups i have actually used and tested

## MK4 Enderwire PrusaSlicer
This is PrusaSlicer 2.6a6 profile for the enderwire based on the Prusa MK4 profiles speeded up a bit.
I'm limiting infill to 120mm/s for ABS, you can set this to 200mm/s if and ride the filament's vol flow limit; this works well with PLA, for ABS I run a bit slower to avoid die shrink issues warping my parts.

If you run into issues, set a parameter i;ve tuned back to the MK4 default and go from there.

This profile is set up for my 0.9 degree high torque steppers running in stealthchop, I can probably go faster, but this is quiet and close to my input shaper speed limits.

I've included my filament presets for eSun ABS+ because it's popular. Tune the extrusion multiplier PER SPOOL. Also 3dTomorrow PLA and 3DQF ABS as they're a little different and I've got them working well.

## MK2 Bear
This is a prusa mk2 frame with a [AfterBEARner](https://www.printables.com/model/54545-afterbearner-the-prusa-bear-afterburner/files) setup for an improved X and to try a Voron stealthburner.

This version is for a Bigtreetech SKR2 MCU and is currently in use as my main ABS printer. 

## Switchwire Ender3 Conversion
This is VS373, it has a creality bed and frame, BTT SKR mini E3 2.0 mcu, BTT filament motion sensor, E3D motors and currently a Revo Voron hotend. I use it as my "nice" PLA printer.

## Dual Extrusion
This is a mod on my ender3 with an afterburner toolhead. Here it's configured with an SKR2, but i've had it working with an SKR mini and a creality 4.2.2 board running the extruders. I used the switchwire multi-extruder bowden adapter. It's likely a mess and I can't verify it works at this moment, but extruder_board.cfg likely has the useful parts.

I've included the printer settings I'm using in super slicer.