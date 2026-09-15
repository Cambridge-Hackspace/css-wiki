# 3D Printers

## Overview
The Hackspace runs a fleet of FDM (Fused Deposition Modeling) 3D printers that build three-dimensional objects layer by layer from digital models. This page is the main reference for using them: rules, safety, slicing, filament, and troubleshooting. Training is required before independent use.

## Printer inventory
The space currently has the following printers.

### Prusa
- 2 Prusa 3.5's

### Bambu
- 1 Bambu A1
- 2 Bambu A1-Mini's
- 1 Bambu X1 Carbon
- 1 Bambu [black one ?]

### Snapmaker
- 1 Snapmaker U1 — see the dedicated guide: [Snapmaker U1](TOOLS/3D-PRINTING/snapmaker-u1.md)

## Training required
To use any of our 3D printers independently, all Hackspace members must first complete in-person training. See [Tool Training](TOOLS/tool-training.md) for how to get certified. In-person training is a hands-on demonstration; you're welcome to bring an `.stl` file you'd like to print, or the trainer can find a demo model with you on [Thingiverse](https://www.thingiverse.com/).

### Classes
- **Intro to 3D Printing:** 1/month — covers *Using the printers* (the pre-training reading below is a prerequisite)
- **Intro to 3D Printer Troubleshooting:** 1/month — covers *Common print failures and fixes*
- **Advanced 3D Printing:** 1/month — covers *Advanced 3D printing / filament types* (Intro classes are prerequisites)
- **Advanced Troubleshooting & Maintenance:** 1/month — covers *Advanced printer maintenance*

## Safety
- **Never touch the nozzle/hotend during or just after printing.** They can reach over 300°C and can give you 3rd degree burns instantly. Allow about 10 minutes to cool down before touching, and monitor temperature on the printer's display.
- Ensure proper ventilation. **All high-VOC filaments are banned** — this includes ABS, ASA, PC, POM, and a few other niche filaments. Confirm your chosen material does not require ventilation before use.
- Allow prints to cool before removing them from the bed. To remove items from the bed, use the chisel/scraper.
- Keep the workspace clear of flammable materials.
- **Do not disassemble any part of the printer** unless you are following the disassembly tutorials. When in doubt, ask for help.
- **Do not use brute force on the printers.** If you are pulling, pushing, or prying and it isn't budging, then it isn't meant to move like that. Brute force is more likely to break the machine than fix your issue.
- You must watch the printer for the first few layers, as this is when most failures happen. If those print successfully, you're welcome to leave for the duration of the print.

### Hackspace printing rules
1. If someone else's finished print is on the printer you want to use, please move it to the "Completed Prints" bin located on the top shelf to the right of the printers.
2. Always clean the heatbed plate with either isopropyl alcohol or dish soap before starting a new print. This is [officially recommended by Bambu Lab](https://wiki.bambulab.com/en/filament-acc/acc/pei-plate-clean-guide).
3. We mostly print PLA and PETG filaments. We have plenty of these in the bins above the printers that you are welcome to use.
4. TPU, Nylon, and Carbon Fiber are also permitted, but they require specific heat settings that need extra consideration and research. Please be extra careful when printing these filaments.
5. **All high-VOC filaments are banned.** This includes ABS, ASA, PC, POM, and a few other niche filaments. Confirm that your chosen material does not require ventilation before use.
6. You must watch the printer for the first few layers, as this is when most failures happen. If those print successfully, you're welcome to leave for the duration of the print.
7. **Never touch the nozzle/hotend during or just after printing** — they can reach over 300°C and cause instant 3rd degree burns. Allow about 10 minutes to cool, and monitor temperature on the display.
8. **Do not disassemble any part of the printer** unless you're following the disassembly tutorials. When in doubt, ask for help.
9. If you have any printing questions or a printer displays an error, leave a message in the [Hackspace Discord](https://discord.gg/sH8UKqdTpH). We're happy to help. 💗
10. **Do not use brute force on the printers.** Be gentle and refer to the troubleshooting guides.
11. At the end of the day, our 3D printers are machines. If you treat them well, they'll treat your projects well.

## Filaments
### Recommended
- PLA
- PETG

### Supported
- TPU (sometimes)
- Nylon and Carbon Fiber (permitted, but require specific heat settings and extra care)

### Filament brands stocked
- Bambu
- Prusament
- Inland
- Sunlu
- eSun

## Background: 3D printing basics
### What is a 3D printer?
A 3D printer creates physical, three-dimensional objects from digital models using additive manufacturing — building items layer by layer rather than cutting material away (subtractive manufacturing). There are two main types: Fused Deposition Modeling (FDM), which melts solid plastic and extrudes it through a small nozzle on a motion system; and SLA (Stereolithography), which uses UV light to cure liquid resin. The Hackspace's printers on this page are all FDM. (For the Hackspace's SLA printer, see [Form 2 SLA 3D Printer](TOOLS/3D-PRINTING/form2-sla-printer.md).)

### What is a 3D printed part?
All 3D-printed parts start as digital models saved as an `.stl` or `.3mf` file. Models can be created in free CAD software such as [Onshape](https://www.onshape.com/en/), [FreeCAD](https://www.freecad.org/) or [Blender](https://www.blender.org/), or downloaded from libraries like [Thingiverse](https://www.thingiverse.com/) or [MakerWorld](https://makerworld.com/en). STL stands for Standard Tessellation Language, the universal standard for 3D CAD models. 3MF (3D Manufacturing Format) is a more modern file type that improves on some of STL's shortcomings.

### Parts of a 3D printer
Below is a diagram of the Bambu Lab A1. While the makerspace has several other printers, many of these components are standard across makes and models.

![Labeled diagram of a Bambu Lab A1 with 15 numbered parts](assets/tools/3d-printer/img02.png)

1. **Printer Frame** — primary structure of the printer.
2. **Toolhead** — houses the hotend and extruder motor.
3. **X-Axis Assembly** — motion system that handles left and right motion.
4. **Purge Wiper** — cleans the nozzle after a filament purge or color change.
5. **Silicone Sock for Hotend** — protects your fingers from getting burned.
6. **Heatbed** — heated metal plate that keeps your part from moving while printing.
7. **Bambu USB-C Cable** — transmits data between mainboard and toolhead.
8. **Filament Cutter Lever** — cuts the half-melted tip off the filament, greatly reducing the risk of a clog.
9. **Live View Camera** — allows remote print monitoring and timelapses.
10. **Z-Axis Leadscrew** — motion system that handles up and down motion.
11. **Part Cooling Fan** — cools filament after extrusion, which helps with overhangs and fine details.
12. **Nozzle** — precisely extrudes molten filament.
13. **Nozzle Wiper** — keeps the nozzle clean and free of gunk that can cause a clog.
14. **Screen** — displays printer information such as nozzle temp, filament colors, print progress, and error codes.
15. **MicroSD Card** — stores all 3D models loaded onto the printer.

### Supports
Sometimes a model has overhangs, bridges, or other floating parts that would be printed mid-air if nothing supported them — an issue for a 3D printer, which cannot print in midair. Supports solve this by printing extra filament underneath these areas, leaving a small gap so they can be removed later. After printing, these scaffolds tear away with pliers or by hand. In general, overhangs of more than 45° need supports.

Below are two of the same model, one printed with supports and one without.

![Two identical T-shaped models side by side; the left printed without supports has a stringy, sagging overhang, the right printed with supports is clean](assets/tools/3d-printer/img03.png)

### Slicing software
Think of a slicer as a translator: it converts the geometry of a 3D model into G-Code, the set of instructions the printer understands. The slicer also lets you adjust position, orientation, size, color, and supports on the print bed, and — using the printer's built-in camera — view, start, or cancel prints remotely.

The Hackspace primarily uses **Bambu Studio**. You're welcome to [install Bambu Studio on your own laptop](https://bambulab.com/en-us/download/studio) before training, but if you'd rather not, it's already installed on the desktop PC next to the CO₂ laser cutter. (The Snapmaker U1 uses **OrcaSlicer** — see the [Snapmaker U1 guide](TOOLS/3D-PRINTING/snapmaker-u1.md).)

![Bambu Studio slicer interface showing a model on the build plate with the filament list and print settings panels](assets/tools/3d-printer/img04.png)

**Shared account login**
- The Bambu Studio shared-account login is available from a trainer or the space's shared credentials store (not published in the wiki).
- The auth code is generated by a bot in the *#bambu-labs-3d-printers* Discord channel. Trained members are added to that channel so they can log in to the shared account from their own devices at any time via the bot's auth code.

### Nozzle sizes
Nozzles come in different sizes. Smaller nozzles produce higher detail and resolution at the cost of speed; larger nozzles print faster at the cost of detail. 0.4mm is the most common size as it balances both. The Hackspace owns 0.2mm, 0.4mm, and 0.6mm nozzles. The X1 Carbon is equipped with a 0.4mm hardened steel nozzle capable of printing carbon fiber filament.

![Print quality comparison of the same model at 0.2mm, 0.4mm, 0.6mm and 0.8mm nozzle sizes, from sharpest to most pronounced layer lines](assets/tools/3d-printer/img05.jpg)

Approximate print times for the same model: **0.8mm** ~20m, **0.6mm** ~30m, **0.4mm** ~50m, **0.2mm** ~3hr. 3D printing is a constant tug-of-war between speed and quality — really high quality takes a really long time to print.

## Finding a 3D model online
- [**Thingiverse**](https://www.thingiverse.com/) — a free online repository of user-submitted 3D models.
- [**MakerWorld by Bambu Lab**](https://makerworld.com/) — similar to Thingiverse but run by Bambu Lab; models can be opened directly in Bambu Studio.
- [**Printables**](https://www.printables.com/) — similar to Thingiverse but run by Prusa; models can be opened directly in PrusaSlicer.
- [**Gridfinity**](https://gridfinity.perplexinglabs.com/) — great for making custom tool organization bins.
- [**Design for 3D-Printing**](https://blog.rahix.de/design-for-3d-printing/) — a blog post compiling popular tips for designing functional parts.
- [**Onshape**](https://www.onshape.com/) — a free browser-based CAD tool for making new models and remixing existing ones. Learning to model takes [less than 30 minutes](https://www.youtube.com/watch?v=aMwLnpVwTXU).

## Using the printers
### Workflow
1. Prepare or download your 3D model (`.stl` or `.3mf`).
2. Slice the model in the appropriate software for the machine: Bambu Studio for Bambu, PrusaSlicer for Prusa, OrcaSlicer for the Snapmaker U1.
3. Load filament and assign its color and type on the printer's touchscreen.
4. Send the print, then watch and monitor the first layer.

### Loading/unloading filament
- [A1 Mini external spool loading](https://wiki.bambulab.com/en/a1-mini/manual/first-print-with-external-spool)
- [AMS Lite spool loading](https://wiki.bambulab.com/en/a1-mini/manual/first-print-with-ams-lite)
- [AMS spool loading](https://wiki.bambulab.com/en/x1/manual/ams-setup-and-filament-loading#step-2-loading-filament-in-the-ams)

### Manually setting bed/nozzle temperature
**A1 & A1 Mini**
- Nozzle temp: tap "Control" → "Nozzle" → type desired temp → "OK"
- Bed temp: tap "Control" → "Bed" → type desired temp → "OK"

**P1S**
- Nozzle temp: Control menu (nozzle icon) → select the nozzle icon (top-most) → adjust to desired temp (up/down for 10° increments, left/right for 1°)
- Bed temp: Control menu (nozzle icon) → select the heatbed icon (2nd from top) → adjust as above

**X1 Carbon**
- Nozzle temp: tap Control menu (2nd icon from top) → "Nozzle & Extruder" → type desired temp → "Confirm"
- Bed temp: tap Control menu (2nd icon from top) → "Heatbed" → type desired temp → "Confirm"

### Surface ironing
Surface ironing improves the smoothness of a print's top layers by letting the hot nozzle pass over the surface multiple times, melting and redistributing filament to fill imperfections. These calibration models help you dial in the optimal settings:
- [Snapmaker U1 ironing calibration model](https://www.printables.com/model/1586194-top-surface-ironing-test-for-snapmaker-u1/files)
- [Bambu Lab ironing calibration model](https://makerworld.com/en/models/175615-ultimate-ironing-test-das-original?from=search#profileId-193062)

### Sending models to a printer
- [Sending a print directly from Bambu Studio](https://youtu.be/lDEGnIYS8lo?si=U1rex56PhwiY_Hez)
- [Printing from an SD card](https://youtu.be/I44wym9EGfw?si=2xojgzeu0ttO27p2)
- [Printing a file stored on the printer directly](https://youtu.be/nTkQ8s7uivA?si=tYp0RXQDRSIAHDgJ)

## Common print failures and fixes
### Model not sticking to build plate
**Looks like:** curled corners, first-layer blowout, or the object detaching mid-print.
**Possible causes:** heatbed too hot or too cold, build plate not cleaned, or bottom surface too small.

- **Bed temperature:** ensure it's correct for the filament — PLA 45–60°C, PETG 70–85°C, TPU 35–50°C.
- **Build plate not clean:** clean with dish soap and water (preferred) or 90%+ isopropyl alcohol (IPA).
  - *Dish soap & water:* spray soap on the plate, scrub with the soft side of a sponge, rinse with water, dry with a clean towel or air dry.
  - *IPA:* spray 90%+ IPA on the plate, wipe with a microfiber towel side-to-side, wait 15–30 seconds to evaporate.
  - Bambu Lab notes detergent is preferred for textured plates: "Alcohol might just spread the oils on the print surface instead of removing it. Detergent acts as a degreaser… to clean it and improve adhesion." ([source](https://wiki.bambulab.com/en/filament-acc/acc/pei-plate-clean-guide))
- **Bottom surface too small:** add a brim to your model ([tutorial](https://www.youtube.com/watch?v=bMpPhOZWvRI)).
- If none of the above works, apply glue-stick glue to the build surface.

### Printer is not extruding
**Looks like:** toolhead floating above the model while printing, or the extruder gear clicking and grinding.
**Possible causes:** clogged nozzle (most common), worn extruder gear, filament sensor failure, or extruder unit board (EUB) failure.

- **Clogged nozzle** (clearing depends on the printer):
  - [A1 Mini nozzle unclogging](https://wiki.bambulab.com/en/a1-mini/troubleshooting/nozzle-clog)
  - [P1S & X1 Carbon nozzle unclogging](https://wiki.bambulab.com/en/x1/troubleshooting/nozzle-clog)
  - [Snapmaker U1 nozzle unclogging](https://wiki.snapmaker.com/en/snapmaker_u1/troubleshooting/known_issues_and_quick_fixes)
- **Extruder gear / filament sensor / EUB failure:** contact the 3D Printing Trainers via the [Hackspace Discord](https://discord.gg/sH8UKqdTpH) so replacement parts can be ordered.

### Sagging/stringy filament on overhangs
**Looks like:** stringy, sagging material on unsupported overhangs (the "forbidden spaghetti").
**Cause:** aggressive overhangs without supports.
**Fix:** [use supports on overhangs greater than 45°](https://youtu.be/KvWCacO7yk4?si=PTYofNAHYo8n9ont).

### Filament snaps inside the PTFE tube
**Looks like:** filament stops feeding despite the spool being installed; fragments visible inside the PTFE tube.
**Causes:** brittle filament or bad luck.

- **Fragments in the tube:** detach the PTFE tube from the printer, shake fragments into the trash, or feed filament from another spool through to push them out.
- **Brittle filament:** keep filament as dry as possible, especially Carbon Fiber or Fiberglass blends.

### PTFE tubes falling out of their sockets
**Looks like:** tubes won't stay seated despite proper insertion.
**Causes:** chewed-up tube ends or bent metal push-fit rings.

- **Chewed ends:** the tube end will look mangled — cut it off (usually a few millimeters is enough).
- **Bent push-fit rings:** bend the metal back into place ([tutorial](https://www.youtube.com/watch?v=hmByMHddxLE)).

### Quick reference
- **First layer not sticking:** re-level the bed, adjust Z-offset (see *Model not sticking to build plate* above).
- **Stringing:** adjust retraction settings; dry the filament.
- **Layer shifting:** check belt tension.

## Advanced printer maintenance
### Detaching & reattaching PTFE tubes on the AMS Lite hub
Push down on the red 3D-printed cap and pull the PTFE tube you want to detach. If you feel resistance (pulling fairly hard and it isn't moving), **immediately stop pulling.** The push-fit ring hasn't released the tube, and continuing will damage the tube, the filament hub, and the toolhead. In that case, slide both parts of the red cap away from the hub and [follow this short tutorial](https://www.youtube.com/shorts/Z_N8zvzk0Nc).

### Disassembling the AMS Lite filament hub
[Follow this guide](https://wiki.bambulab.com/en/a1/maintenance/filament_hub_cleaning). **When to do this:**
- **Manual loading resistance:** significant obstruction when manually feeding filament into the hub.
- **AMS feed failure:** filament visibly reaches the hub but the printer shows "Unable to feed filament into the extruder," and the filament sensor doesn't trigger (no green dot on the toolhead icon).
- **False positive sensor:** toolhead icon shows a constant green dot even with no filament loaded.

You'll need H1.5 and H2.0 Allen keys and flat tweezers.

### Flattening push-fit rings
To flatten the metal push-fit rings that secure PTFE tubes in the filament hub, [follow this guide](https://wiki.bambulab.com/en/a1/maintenance/filament_hub_cleaning). Do this when PTFE tubes stop staying seated in the AMS Lite hub. You'll need flat tweezers.

### Disassembling the extruder units
- [Disassemble the P1S extruder unit](https://www.youtube.com/watch?v=8MmZrdQF6wM)
- [Disassemble the A1-series extruder unit](https://www.youtube.com/watch?v=kUJYCWbFxLk) — do this *carefully*, as it's easy to break the filament sensor's ribbon cable.

## Advanced 3D printing: filament types
> Work in progress. The following covers filament chemistry in more depth. Additional advanced topics (infill types, direct drive vs Bowden, bed slinger vs CoreXY, multicolor printing) are not yet written up.

### Polylactic Acid (PLA) — very easy to print, not very strong
- **Cost:** ~$15–$25/kg. **Strength:** low — you can break it with your bare hands.
- **Pros:** easy to print, cheap, available in the most colors.
- **Cons:** lower heat resistance (can soften in a hot car), not very strong, brittle (snaps and shatters), degraded by UV light.
- **Printing:** 190–230°C nozzle, 50–60°C bed. Hardened nozzle / enclosure / ventilation all optional.
- **Variants:** PLA+ (tougher), Silk PLA (shiny, slightly weaker), Glow PLA, Wood-filled (sandable/stainable), Metal-filled (denser, metallic), PLA-CF (carbon fiber, stiffer, lower warping), HT-PLA (higher temperature resistance).

### Polyethylene Terephthalate Glycol (PETG) — the default for most makers
- **Cost:** ~$20–$35/kg. **Strength:** fairly strong — breaking it barehanded is possible but not easy.
- **Pros:** stronger than PLA, much less brittle, much better heat resistance.
- **Cons:** hygroscopic (absorbs moisture, affecting print quality), prone to stringing and oozing, high shrinkage (poor for tight dimensional accuracy).
- **Printing:** 230–260°C nozzle, 70–85°C bed. Hardened nozzle / enclosure / ventilation all optional.
- **Variants:** PETG+ (stronger, more heat resistant), Transparent PETG, Glow PETG, PETG-CF (carbon fiber), HF PETG (high flow, faster).

### Acrylonitrile Butadiene Styrene (ABS) / Acrylonitrile Styrene Acrylate (ASA) — banned at the Hackspace
> ABS and ASA are **high-VOC and banned** at the Hackspace. Documented here for reference only.

- **Cost:** ~$20–$30/kg. **Strength:** pretty strong — you'll need a hammer/bat to break it.
- **Pros:** very impact resistant, very chemically resistant (outdoor-capable), more heat resistant than PETG.
- **Cons:** hygroscopic, strong warping, emits styrene fumes when printing (styrene fumes + lungs = pneumonia).
- **Printing:** 230–260°C nozzle, 90–110°C bed. Hardened nozzle, enclosure, and ventilation all **required**.
- **Variants:** ABS+ (higher strength/heat resistance), ABS-CF (carbon fiber), ABS-GF (glass fiber, lighter).

### Thermoplastic Polyurethane (TPU) — a filament that put all its points into Dexterity
- **Cost:** ~$25–$35/kg. **Strength:** impacts do nothing, but it can be cut with bolt cutters; hand strength won't get far.
- **Pros:** very high impact resistance, extremely elastic.
- **Cons:** very hygroscopic (high-temp drying required), cannot print fast, prone to stringing.
- **Printing:** 210–240°C nozzle, 30–60°C bed. Hardened nozzle / enclosure / ventilation all optional.
- **Variants:** TPU-CF (carbon fiber, higher tensile strength).

### Nylon / Polyamide (PA) — a filament by engineers for engineers
- **Cost:** ~$30–$60/kg. **Strength:** very strong — only breakable with tools like bolt cutters or a hydraulic press.
- **Pros:** very high impact resistance, very high tensile strength, very high chemical resistance.
- **Cons:** very hygroscopic (high-temp drying required), extremely prone to warping (more than ABS), very difficult to print.
- **Printing:** 240–290°C nozzle, 70–100°C bed. Hardened nozzle, heated enclosure (55+°C), and ventilation all **required**.
- **Variants:** Nylon-CF (carbon fiber), Nylon-GF (glass fiber, lighter), PA12 ("easy mode nylon," less hygroscopic and less warp-prone).

### Polycarbonate (PC) — the roughest, toughest filament you can buy
> PC is **high-VOC and banned** at the Hackspace. Documented here for reference only.

- **Cost:** ~$35–$60/kg. **Strength:** extremely strong — bats and bolt cutters do nothing; you'd need a sledgehammer or a 9mm round.
- **Pros:** chart-topping impact, tensile, and chemical/heat resistance.
- **Cons:** extremely hygroscopic (high-temp drying required), extremely prone to warping (more than nylon), notoriously difficult to print.
- **Printing:** 280–320°C nozzle, 110–120°C bed. Hardened nozzle recommended; heated enclosure (80+°C) and ventilation **required**.
- **Variants:** PC-CF (carbon fiber, stiffer, lower warping).

## Remote printing
- **OctoPrint / SimplyPrint (Prusa):** remote printing to the Prusa via the OctoPrint server. Setup and member onboarding is documented on [3D printer remote printing](TOOLS/3D-PRINTING/3d-printer-remote.md).
- **Bambu / Snapmaker:** remote monitoring, starting, and stopping prints is done through Bambu Studio / OrcaSlicer's device tab using the shared account (see *Slicing software* above and the [Snapmaker U1 guide](TOOLS/3D-PRINTING/snapmaker-u1.md)).

## Training checklist (for trainers)
Criteria a Hackspace member should be taught to use the 3D printers independently — rules, safety, basic usage, and common troubleshooting. Members are expected to understand how to perform basic repairs when needed.

1. Ensure participants have read the *Hackspace printing rules* above.
2. Printer station tour: which printer models we have; where the free PLA is (bins above the printers); what AMS and AMS Lite do; the multi-material capabilities of the Snapmaker U1 and Bambu AMS; where the soap + sponges and alcohol bottles are; where the pliers and build-plate glue are; the difference between smooth and textured print beds; the filament dryers and what they do.
3. Using the slicer: log into the shared account (see *Slicing software*); get the auth code from the Discord bot; add **all trained members** to the 🖨️ bambu-lab-3d-printers channel so they can log into the shared account from their own devices; open an STL into a new project; scale, orient, duplicate, auto-align, cut, and enable supports; paint a model for multiple colors/types; add a brim or raft for poor adhesion; enable supports for overhangs; select the printer and nozzle; slice files; use the preview tab to view layer-by-layer; send and export sliced files; remotely view and stop prints in the device tab.
4. Show how to load and unload filament from the printers, AMS Lite, and AMS (each AMS loads a bit differently).
5. Stress assigning filament color and type (PLA, PETG, etc.) to each loaded filament on the touchscreen, so members starting prints remotely know what's loaded.
6. How to clean the print bed with soap and water when greasy.
7. How to change nozzles (0.2mm, 0.4mm, 0.6mm) on the Bambu printers.
8. How to properly remove PTFE tubes from the AMS Lite hub to clear broken filament: push down the red cap to release the push-fit rings; while holding it down, pull the stuck tube out (no resistance); feed a separate piece of filament into the opposite end to push out the broken part; push the cap down again, slot the tube back in, release; tug lightly to confirm it's secure.
9. How to clear a filament clog inside the extruder unit, the AMS, and a nozzle. Members are responsible for fixing these when they occur.
10. Solving common printing problems: see *Common print failures and fixes* above.

## Tips
- Seal PLA in a bag when not in use — if it absorbs too much moisture from the air it will get brittle.
- Make a nice flat bed of 3M painter's tape for your prints — make sure each pass doesn't overlap.
- To remove items from the bed, use the chisel.

### Legacy notes (older self-built printer)
> These notes predate the current Bambu/Prusa fleet and refer to a self-built printer running Repetier/Marlin. Kept for historical reference.

- Make sure you use the little white insert to guide the PLA into the extruder — it keeps the filament centered on the extrusion gear for best accuracy.
- Configure Repetier and the slicer for a bed size of 100mm × 100mm, nozzle width 0.4mm, 200°C.
- Be careful of the Z limit switch — the wires in the back are loose, and if they get in the way the machine won't find its Z home position, resulting in a lot of belt twisting.
- The default EEPROM settings in the Marlin firmware (https://github.com/ErikZalm/Marlin) tell the printer how many steps of each motor are needed per direction. The defaults are probably OK, but this printer used `M92 X110.00 Y110.00 Z2020.00 E98.00` (tested with a micrometer in June 2014).
- To load PLA, the hot end must be hot. Plug in everything and set the temperature to 200°C. Once warm, loosen the fan assembly and manually feed the PLA down into the hot end until some squirts out the bottom, then carefully replace the fan assembly to provide tension against the extrusion gear.

## Resources
- [Snapmaker U1 guide](TOOLS/3D-PRINTING/snapmaker-u1.md)
- [3D printer remote printing (OctoPrint / SimplyPrint)](TOOLS/3D-PRINTING/3d-printer-remote.md)
- [Form 2 SLA 3D Printer](TOOLS/3D-PRINTING/form2-sla-printer.md)
- [Tool Training](TOOLS/tool-training.md)
- [Hackspace Discord](https://discord.gg/sH8UKqdTpH)
