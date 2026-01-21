# 3D Printer

## Overview
FDM (Fused Deposition Modeling) 3D printer for creating three-dimensional objects from digital models.

The space currently has the following printers

### Prusa

- 2 Prusa 3.5's

### Bambu

- 1 Bambu A1
- 2 Bambu A1-Mini's
- 1 Bambu X1 Carbon
- 1 Bambu [black one ?]

## Recommended Filaments

- PLA
- PETG

## Supported Filaments

- TPU (Sometimes)

## Filament Brands

- Bambu
- Prusament
- Inland
- Sunlu
- eSun


## Safety Guidelines
- Never touch the hot end or heated bed during/after printing
- Ensure proper ventilation, especially when printing ABS
- Allow prints to cool before removing
- Keep workspace clear of flammable materials

## 3d Printing Workflow
1. Prepare your 3D model (STL file)
2. Slice the model using appropriate software, for the machine in question. For Bambu, BambuStudio; Prusa, Prusalicer
3. Load filament
5. Start the print and monitor the first layer

## Training Required !!!
See [Tool Training](./tool-training.md) for information on getting certified to use this equipment.

## Resources
- Print settings guide: [To be added]

## Maintenance
- TODO

## Troubleshooting
- **First layer not sticking**: Re-level bed, adjust Z-offset
- **Stringing**: Adjust retraction settings
- **Layer shifting**: Check belt tension

## TIPS

- Seal up the PLA in a bag when not in use -- if it gets too much water from the air it will get brittle
- Make sure you use the little white insert to guide the PLA into the extruder -- it helps to keep the filamenbt in the middle of the extrusion gear and ensures the best accuracy.
- Make a nice flat bed of 3M painters tape for your prints -- make sure each pass doesn't overlap
- Configure Repetier and slicer for a bed size of 100mm by 100m, nozzle width of 0.4mm, 200C
- Be careful of the Z limit switch -- the wires in the back are loose and if they get in the way the machine will not find its Z home position and lots of belt twisting will result
- The default EEPROM settings in the Marlin firmware (https://github.com/ErikZalm/Marlin) tell the printer how much steps of each motor are needed for each direction. The defaults are probably OK, but I actually use "M92 X110.00 Y110.00 Z2020.00 E98.00" (Tested with a micrometer in June 2014)
- To load PLA, the hot end must be hot. Plug in everything and click "set temperature" to 200 degrees. Wait until it gets warm and then loosen the fan assembly and manually feed the PLA down into the hot end extruding chamber until some starts to squirt out the bottom. Then replace the fan assembly carefully to provide tension against the extrusion gear.
- To remove items from the bed, use the chisel
