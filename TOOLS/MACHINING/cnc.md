# CNC Machine (Carvera)

## Overview

Computer Numerical Control (CNC) machine for precision cutting, carving, and milling of various materials. The Hackspace's CNC machine is the **Carvera**, a desktop CNC mill. It can precisely mill wood, plastic, and metal, and can also be used to manufacture PCBs.

![The Carvera desktop CNC mill](assets/tools/cnc/img02.png)

## Safety
- Double-check that the spindle column has a spin command such as `M3` in your toolpaths, or you may break an endmill by smashing it into your material while it is not spinning.
- When setting the stock size, give yourself margin against the stock mounts. If the stock width/depth is set too low, the tool will crash into the mount.
- Shaft diameter and width matter because of deep cuts. Always undershoot.
- Step-over is very important for harder materials.

## The Three Pieces of Software

To use the Carvera, you need three pieces of software:

1. **CAD (Computer-Aided Design)** to design the part you want to make.
   - Many members use Onshape, a browser-based tool with a strong free tier.
   - Other tools include FreeCAD, TinkerCAD, Fusion 360, or SolidWorks.
2. **CAM (Computer-Aided Manufacturing)** software to generate tool paths from the part geometry. This is the main focus of this guide (see [KiriMoto](#kirimoto) below).
3. **Carvera Controller** to connect to the mill and execute toolpaths.
   - It is installed on the computer to the left of the mill.
   - It has [pretty solid docs](https://wiki.makera.com/en/carvera/manual/software) for when you get to this step.

### CAM software options

- [MakeraCAM](https://wiki.makera.com/en/software/MakeraCAM_userguide) is designed to work with the Carvera. It is a closed-source tool and is on the PC next to the Carvera. It is fully featured, but is very frustrating to actually use.
- **Fusion 360** also has CAM tools that support the Carvera, but many features are paywalled and, reportedly, tool change does not work.
- [KiriMoto](https://grid.space/kiri/) is free, open-source, and can directly connect to Onshape. It is the tool described in detail below, though the other two have been used by other Hackspace members.

## KiriMoto

### Setup

KiriMoto is available as an [Onshape application](https://cad.onshape.com/appstore/apps/CAM/568c6d69e4b0d556c8625e5b), in the [browser](https://grid.space/kiri/), or as an [independent download](https://grid.space/downloads.html). All three are identical; the Onshape application just makes it slightly easier to import models and save settings.

If you want to use KiriMoto through Onshape, click the +, go to Applications, and search for it in the app store if it is not already installed. It should then appear under Applications.

![Adding KiriMoto in Onshape](assets/tools/cnc/img03.png)
![KiriMoto in the Onshape app store](assets/tools/cnc/img04.png)
![KiriMoto under Applications](assets/tools/cnc/img05.png)

First select **CNC** from the Mode dropdown. From Setup select Machines, and then from Select Device select **Makera.Carvera**.

![Selecting the Makera.Carvera device](assets/tools/cnc/img06.png)

Double-check the spindle column has a command like `M3` in it, or else you may break an endmill by smashing it into your material while it does not spin.

![Spindle command column](assets/tools/cnc/img07.png)

Input your tools in Setup > Tools:
- **Type** - what kind of tool. Most of what we have are flat ends.
- **Tool #** - what position on the tool changer the tool is in.
- **Shaft diameter** - 0.125 in, the shaft size for the Carvera.
- **Flute diameter** - how wide your tool is.
- **Taper angle and tip** - specified on the box of any angled bit.
- **Length** doesn't matter; the Carvera re-measures the end position of tools when it picks them up.

Hit + and repeat this process for any additional tools you need, then save.

### Making toolpaths

![Loading a part in KiriMoto](assets/tools/cnc/img08.png)

Load the target part with File > Import.

![Imported part](assets/tools/cnc/img09.png)

The only section of the left-side windows to modify is **Stock**. Increase the width and depth to several times the diameter of your endmill to give margin against the stock mounts. If this value is set too low, you will crash into the mount. Set height to 0 if, for example, you are machining a 3mm thick part out of 3mm acrylic.

![Stock settings](assets/tools/cnc/img10.png)
![Stock margin around the part](assets/tools/cnc/img11.png)

On the right side of the map, hit + to add Operations. Add a **Rough** pass to cut out the internal geometry, followed by an **outline** pass to finish cutting out the part. (For more 3D parts, try Contour or a roughing pass with a smaller step-down size.)

**Make sure to set the Feeds and Speeds.** The Makera wiki has a [useful reference table](https://wiki.makera.com/en/speeds-and-feeds) of values by bit and material.

You can also include steps here to add mating pegs and flip the part over, though that is beyond the scope of this guide.

![Operations and feeds/speeds](assets/tools/cnc/img12.png)

KiriMoto has a nice animation tool. Watch it and enjoy how far you've come.

![KiriMoto toolpath animation](assets/tools/cnc/img13.png)

Hit export at the top and select gcode. You can load this into [Carvera Controller](https://wiki.makera.com/en/carvera/manual/software) and run it.

## Tooling (Endmills)

Tooling is a consumable, so you should buy your own. The Hackspace may have donated or abandoned tooling of unknown quality (which may have been misused or damaged) available to help you get started - we're still figuring this out.

- For soft materials (plastic), Carvera recommends single-flute endmills (one cutting spiral).
- The Carvera has tool holders for 1/8" (0.125") tooling. (To do: check if we have other sizes.)

### What's an endmill?

It's like a drill bit that cuts sideways. Some endmills are *only* good at cutting sideways, although this matters more for hard materials like metals, so make sure the type of path makes sense for the endmill being used.

### Where can you buy endmills?

- Tiny endmills, excellent quality: <https://www.lakeshorecarbide.com/2flute-2.aspx>
- Pretty much anything, excellent quality: <https://www.mcmaster.com/products/end-mills/>
- Example online marketplace listing (quality may vary greatly between sellers and products): <https://www.amazon.com/Genmitsu-Carbide-Woodworking-Cutting-OS10A/dp/B0CKZ7HZGB>

![Example endmill product listing](assets/tools/cnc/img14.jpg)

## Using Bit Collars

The Carvera has an automatic tool changer that picks up endmills with bit collars on them. There are different sizes: <https://www.makera.com/products/bits-collar>. We only have 1/8" bits.

If you need to add a collar to a bit, grab a spare collar and the collar tool. Makera has a great video on how to do this: [How to Install and Remove Bit Collars](https://www.youtube.com/watch?v=J8edCDsmz8I).

![Installing a bit collar](assets/tools/cnc/img15.png)

## Notes from First Training

![Training note - tooling](assets/tools/cnc/img16.png)

Shaft diameter and width matter because of deep cuts. Always undershoot.

![Training note - step over](assets/tools/cnc/img17.png)

Step-over is very important for harder materials.

[Training Onshape workspace](https://cad.onshape.com/documents/8a612e2d765281c3a8c3dfb8/w/b185169372a4ad84476d3f8c/e/8a4ae356769e319d864ea93c?renderMode=0&uiState=6a6015a974760c08754722bd)

## See Also
- [Tool Training](TOOLS/tool-training.md)
