# Snapmaker U1

## Overview
The Snapmaker U1 is one of the Hackspace's FDM 3D printers. This guide is a reference for trainers and trainees who have completed in-person training; it mainly highlights the differences between the Snapmaker and the Bambu printers. We recommend completing the [Bambu printer training](TOOLS/3D-PRINTING/3d-printer.md) first, since this guide builds on it.

## Safety and etiquette
1. Stay near the printer for the first few layers — this is when most failures happen.
2. Never touch the hot end or nozzle during or just after printing — they reach over 200°C. Allow about 10 minutes to cool down.
3. If another person's completed print is left behind, feel free to move it aside to use the printer.
4. Always clean the plate with soap and water before you start a new print.
5. If changing print temperatures, remain present for the entire print. Adjusting temperatures can cause clogs or unexpected printer behavior.
6. ABS, ASA, Acetal (POM), and some other filaments can produce dangerous fumes or particles — **thus they are banned.** Confirm that your chosen material does not require ventilation before use.
7. We mostly print PLA and PETG. TPU, Nylon, and carbon fiber are also permitted, but require specific heat settings you'll need to research or ask about in the Discord.
8. If you have general printing questions or anything weird happens with a printer, leave a message in the Hackspace Discord. Sometimes things break — no worries. ♥️

## What makes the Snapmaker U1 great
One of the key advantages of the Snapmaker U1 is its **toolhead swapping system.** It makes multicolor printing much faster and lets you easily print with multiple materials at a time. Here's a good guide on multimaterial printing: <https://www.youtube.com/watch?v=-2K67P5L8A4>

## Using OrcaSlicer
OrcaSlicer is the open-source version of Bambu Studio and connects to the Snapmaker U1. The interface is almost identical. To add the Snapmaker U1:

1. Ensure you're on the chack wifi and open OrcaSlicer.
2. In the *Prepare* tab, under *Printer*, click the dropdown and select *Add Printer*.
3. Find the Snapmaker U1 and add it.
4. Ensure it's selected from the *Printer* dropdown.
5. Click the green wifi icon next to the dropdown.
6. Ensure the connection type is set to *Octo/Klipper* and set the IP to the Snapmaker's address (shown on the printer; ask a trainer if unsure).
7. Click *Test*. A popup should confirm the connection is working.
8. That's it — when you click print, the print is sent to the Snapmaker.

**Forgot your laptop?** OrcaSlicer is also installed on the PC next to the CO₂ laser cutter. You can download it here: <https://www.orcaslicer.com/>

## Loading and unloading filament
Video tutorial: <https://www.youtube.com/watch?v=UMmymmGDLiY>

## Sending 3D models to the printer
- Send prints directly from Bambu Studio to a Bambu Lab printer: <https://youtu.be/lDEGnIYS8lo?si=U1rex56PhwiY_Hez>
- Print from an SD card: <https://youtu.be/I44wym9EGfw?si=2xojgzeu0ttO27p2>
- Print using a file stored on the printer: <https://youtu.be/nTkQ8s7uivA?si=tYp0RXQDRSIAHDgJ>

## Common print failure fixes
| Problem | Cause | Solution |
| --- | --- | --- |
| Stringy prints or filament frequently snaps | Moist filament | Use a filament dryer. They're located underneath the second A1 Mini. |
| The nozzle bumps the model mid-print, shifting it on the bed | Dirty bed, or small base / tall or unbalanced geometry | Clean the print bed with dish soap or alcohol. For tricky prints, apply glue to the bed ([video](https://www.youtube.com/watch?v=vRcz8tuGcJU)). If the part has a small base or is tall, add a brim or raft in the slicer to increase bed contact ([video](https://www.youtube.com/watch?v=bMpPhOZWvRI)). You can also slice the part into segments and join them with connectors ([video](https://www.youtube.com/watch?v=jsVYz19foq0)). |
| The printer failed to extrude filament | Clogged nozzle | Clogs **inside** the nozzle ([video](https://youtu.be/KvWCacO7yk4?si=PTYofNAHYo8n9ont)). Clogs **outside** the nozzle ([video](https://youtu.be/-bYwgUPOIq8?si=KxqpRq6YaNVD5H8Y)). |
| Sagging filament at overhangs | No supports | Enable supports for overhangs > 45° ([video](https://www.youtube.com/watch?v=_GN4yYcf22A)). You can also slice the part into segments and join them with connectors or super glue ([video](https://www.youtube.com/watch?v=jsVYz19foq0)). |
| Filament snaps inside the PTFE tube | Moist filament | 1. Detach the tube containing the broken filament. 2. This [video](https://www.youtube.com/shorts/Z_N8zvzk0Nc) shows how to correctly detach and re-attach the PTFE tubes. 3. From the opposite end of the tube, load another piece of filament to push out the broken pieces. |
| PTFE tubes are falling out | Push-fit rings are likely bent | Flatten the push-fit rings ([video](https://www.youtube.com/watch?v=hmByMHddxLE)). |

## Finding 3D models online
| Website | Description | Link |
| --- | --- | --- |
| Thingiverse | A free online repository of user-submitted 3D models. | <https://www.thingiverse.com/> |
| Bambu Lab MakerWorld | Similar to Thingiverse but run by Bambu Lab; models open directly in Bambu Studio. | <https://makerworld.com/> |
| Gridfinity | Great for making custom tool organization bins. | <https://gridfinity.perplexinglabs.com/> |
| Printables | Another massive model repository (run by Prusa). | <https://www.printables.com/> |
| Design for 3D-Printing | A blog post compiling popular tips for designing functional parts. | <https://blog.rahix.de/design-for-3d-printing/> |

## Learn to make your own models with Onshape
Onshape is a free browser-based CAD tool for making new models and remixing existing ones. Official site: <https://www.onshape.com/>. Beginner tutorial (25 minutes): <https://www.youtube.com/watch?v=aMwLnpVwTXU>

## Smoothing PLA to a smooth surface
- <https://www.instructables.com/How-to-Smooth-PLA-3D-Prints/>
- <https://www.3dsourced.com/rigid-ink/how-to-smooth-pla-to-a-mirror-finish/>

## What training should cover
1. Safety and etiquette (above).
2. Printer station tour: which Bambu Lab printers we have; where the free PLA is (bins above the printers); each printer's AMS and multicolor capabilities; where the soap + sponges and alcohol bottles are; where the pliers, glue, and bed scraper are; where the smooth and textured print beds live; the filament dryers.
3. Using the slicer: log into the shared account (see [3D Printers](TOOLS/3D-PRINTING/3d-printer.md)); get the auth code from the Discord bot; open an STL into a new project; select the printer and nozzle; resize, rotate, and move objects on the bed; enable supports (needed any time an overhang is > 45°); slice files; use the preview tab; send and export sliced files; remotely view and stop prints in the device tab. If you forgot your laptop, the slicer is installed (with the shared account) on the computer next to the CO₂ laser cutter.
4. Show trainees how to load and unload filament from the printers, AMS Lite, and AMS.
5. Demonstrate assigning filament color and type to each loaded filament on the touchscreen.
6. How to clean the print bed with soap and water before each print.
7. How to change nozzles (0.2mm, 0.4mm, 0.6mm).
8. How to properly remove PTFE tubes from the AMS Lite hub to clear broken filament: push down the white cap to release the push-fit rings; while holding it down, pull the stuck tube out (no resistance); feed a separate piece of filament into the opposite end to push out the broken part; push the white cap down again, slot the tube back in, release; tug lightly to confirm it seats correctly. [Video tutorial](https://www.youtube.com/watch?v=e707GKu_OCs).
9. Solving common printing problems: stringy filament (needs drying); filament clogged inside the hot end; filament clogged outside the hot end; print not sticking to the bed (clean the bed and *maybe* use glue).

## Resources
- [3D Printers (main guide)](TOOLS/3D-PRINTING/3d-printer.md)
- [Tool Training](TOOLS/tool-training.md)
- [Snapmaker U1 known issues & quick fixes](https://wiki.snapmaker.com/en/snapmaker_u1/troubleshooting/known_issues_and_quick_fixes)
