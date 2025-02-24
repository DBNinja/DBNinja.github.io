---
title: Getting Started Guide
description: 
draft: "false"
---
Honestly, just watch the [Teaching Tech](https://www.youtube.com/watch?v=T-Z3GmM20JM) video here. It is good for beginners. 
	This video is about the Ender 3, which is good because this printer (Ender 3 V2) is an upgrade to it and is mostly similar.
	He goes into depth on the parts and details on how to build the printer in the first 10ish minutes of the video (if you want, you can skip it, but it does tell you a lot about the parts in it). 
	Then he goes into depth about 3D Printing, and talks about the software. He uses Ultimaker Cura, but I use Prusaslicer. I don't 100% know how Cura works, but it should at least run okay?
	He also talks about leveling, which is VERY IMPORTANT for 3D Printing. On the plus side, my printer has a a lot of mods to make this easy. Just follow the levelling guide below.
	


Power Supply is different and is at the bottom
The screen on the V2 is better
I have "custom firmware" installed on the printer
The Z axis motor is on the top.
My printer is now a "direct drive"





https://old.reddit.com/r/3Dprinting/wiki/gettingstarted

The software I use: https://www.prusa3d.com/prusaslicer/


## General Leveling instructions:
- Heat up bed to 70C
- Use Tramming Wizard to make sure bed is level (it will tell you which corners to raise/lower)
- Run the auto bed level tool on the printer.
- Save the mesh
- After all of this, you'll want to make sure the Z Offset is set up properly. You can follow Teaching Tech's process with the paper, but I find using a feeler gauge helps me more. Basically you make sure everthing is hot, then make sure that it's just low enough to scratch the paper/feeler gauge (at 0.1 or 0.15 mm)
	- Though his points about squish matter as well. You might want to follow the [first layer squish guide](https://ellis3dp.com/Print-Tuning-Guide/articles/first_layer_squish.html) from Ellis' Print Tuning Guide.


## Tuning
If you want to make your 3D Printer the best it can be, I recommend following [Printer Tuning Guide](https://ellis3dp.com/Print-Tuning-Guide/). Luckily I've already done that with my printer. You do need to change certain settings depending on the filament (like temp, cooling, and maybe flow rates)


Now that you're done, you can check out my [[Upgrades]].
If you're at the point of setting everything up, you can check out my [[Custom G-Code (add this to your slicer)|Prusaslicer G-Code]] or the [[Printer Settings (In PrusaSlicer)|Prusaslicer Settings I use]].
