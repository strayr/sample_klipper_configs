# Really Simple Macros

These should be a bare minimum to get a printer up and running, with very little interdependence, the goal here is readability and reuse of stock functionality. It's assumed the user has a thereabouts functinal config capable of pushing plastic.

## See Also
- [klipper's sample macros](https://github.com/Klipper3d/klipper/blob/master/config/sample-macros.cfg) These are often a good place to start
- [mainsail's default macros](https://github.com/mainsail-crew/mainsail-config)

## Goals:

- PRINT_START including a compatibility wrapper for START_PRINT **done**
- PRINT_END **done**
- PRINT_CANCEL **done**
- PAUSE
- PARK -> Consider the mainsail macros
- M600 -> this is pause + park, if your pause already moves the toolhead, this is easy
- Line purge **done**
  
## Slicer Gcode

### Prusa Slicer

Start Gcode
```
;M104 S0
;M140 S0
START_PRINT EXTRUDER_TEMP=[first_layer_temperature] BED_TEMP=[first_layer_bed_temperature]

```
End Gcode
```
END_PRINT
```
### Orca Slicer

Start Gcode
```
;ORCA custom start print
;M140 S[bed_temperature_initial_layer_single] ; set bed temp
;M104 S[nozzle_temperature_initial_layer] ; set extruder temp

START_PRINT EXTRUDER_TEMP=[nozzle_temperature_initial_layer] BED_TEMP=[bed_temperature_initial_layer_single] 
;end ORCA
```
End Gcode
```
END_PRINT
```