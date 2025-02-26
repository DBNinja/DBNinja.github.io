---
title: Custom G-Code
description: G-Code I added in PrusaSlicer for my modded Ender 3v2
draft: "false"
---


Starting G-Code

```
G90 ; use absolute coordinates
M83 ; extruder relative mode
M104 S150 ; set temporary nozzle temp to prevent oozing during homing
M140 S{first_layer_bed_temperature[0]} ; set final bed temp
G4 S30 ; allow partial nozzle warmup
G28 ; home all axis
G29 A     ; Load UBL
G29 J
G1 Z50 F240
G1 X2.0 Y10 F3000
M104 S{first_layer_temperature[0]} ; set final nozzle temp
M190 S{first_layer_bed_temperature[0]} ; wait for bed temp to stabilize
M109 S{first_layer_temperature[0]} ; wait for nozzle temp to stabilize
G1 Z0.28 F240
G92 E0
G1 X2.0 Y140 E10 F1500 ; prime the nozzle
G1 X2.3 Y140 F5000
G92 E0
G1 X2.3 Y10 E10 F1200 ; prime the nozzle
G92 E0
```


Ending G-Code
```
{if max_layer_z < max_print_height}G1 Z{z_offset+min(max_layer_z+2, max_print_height)} F600 ; Move print head up{endif}
G1 X5 Y{print_bed_max[1]*0.85} F{travel_speed*60} ; present print
{if max_layer_z < max_print_height-10}G1 Z{z_offset+min(max_layer_z+70, max_print_height-10)} F600 ; Move print head further up{endif}
{if max_layer_z < max_print_height*0.6}G1 Z{max_print_height*0.6} F600 ; Move print head further up{endif}
M140 S0 ; turn off heatbed
M104 S0 ; turn off temperature
M107 ; turn off fan
M84 X Y E ; disable motors

```

If you're feeling spicy, you can add this to your Ending G-Code (after the last line) to let you know when a print is complete.
```
M300 P155 S523
G4 P155
M300 P139 S523
G4 P139
M300 P143 S523
G4 P143
M300 P425 S523
G4 P425
M300 P145 S415
G4 P145
M300 P138 S196
G4 P138
M300 P142 S185
G4 P142
M300 P425 S466
G4 P425
M300 P157 S523
G4 P157
M300 P139 S0
G4 P139
M300 P143 S466
G4 P143
M300 P1292 S523
G4 P1292
```
