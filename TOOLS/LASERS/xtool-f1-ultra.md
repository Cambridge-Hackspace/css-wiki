# xTool F1 Ultra

![xTool F1 Ultra](assets/tools/xtool-f1-ultra/img01.png)

## Overview

The xTool F1 Ultra is a laser engraver with a 20W IR (fiber) laser that can
engrave metals, and a 20W blue (diode) laser for marking other materials. It uses
small mirrors that rotate to direct the beam, so it can move the laser dot very
quickly, and it is good for detailed engraving like pictures. It can cut very thin
metals, or thin wood and some other materials. Generally the
[CO₂ laser cutter](TOOLS/LASERS/INDEX.md) is better for cutting things,
except for metals.

This is a separate desktop machine from the CO₂ laser cutter.

### Links

- Manufacturer product page:
  <https://www.xtool.com/products/xtool-f1-ultra-20w-fiber-diode-dual-laser-engraver>
- Official training videos and other info: <https://support.xtool.com/product/33>

## Safety

Before using the xTool F1 Ultra, users must read the safety guide fully. Users
must pass a safety quiz before operating the machine, so please take your time
reading it and ask any questions that you may have.

- Manufacturer safety info:
  [xTool F1 Ultra Safety First (Important)](https://support.xtool.com/article/1366?from=xTool+F1+Ultra&url=/product/33)

### Laser safety

There are two models of the xTool F1 Ultra. One is always considered a class 1
laser (safe). However, the machine that we received can be a class 4 laser
(dangerous) if it is operated with the protective enclosure lifted. The model that
we have also has a slightly more powerful red indicator laser — 0.5mW instead of
0.39mW — so it is a class 2 laser (could hurt you if you stare into it). Don't
stare into the laser beam.

We only operate the laser in conditions where it qualifies as a class 1 or 2
laser device (safe, or relatively safe). It is possible to operate the laser as a
class 4 laser device (dangerous to anyone who can see it) if the protective
enclosure interlock switch is tampered with or otherwise disabled. So, to use the
machine you must agree to only operate it in conditions where it qualifies as a
class 1 or 2 laser device. This means:

- The protective enclosure must be fully closed during operation.
- The protective enclosure interlock must be enabled and functioning normally, so
  that the laser will stop if the protective enclosure is opened.
- Any accessories that require the protective enclosure to be open during
  operation, such as the conveyor belt, cannot be used at the hackspace.
- Do not stare into the indicator laser.

### Materials safety

In general the safe materials are similar to the CO₂ laser, where anything that
produces harmful fumes like ABS or anything with chlorine cannot be used.
However, some metals can be engraved. Aluminum, copper, steel, and brass are the
most commonly used metals. Don't engrave dangerous metals like lead, cadmium,
chromium, manganese, and beryllium
([metal laser cutting hazards](https://ipsystemsusa.com/understand-the-different-fumes-when-laser-cutting/#:~:text=Metal%20Laser%20Cutting%20Hazards)),
anything radioactive, etc.

Rocks that contain silica (granite, sandstone, etc.) may produce crystalline
silica (dangerous) when engraved with a fiber laser. Different sources
([Thunder Laser](https://www.thunderlaserusa.com/blog/can-you-laser-engrave-granite/#is_granite_safe_to_laser_engrave),
Epilog) have conflicting information about the safety of engraving stone
containing silica, and a CO₂ laser may be safer since it melts the stone.

### Fire safety

The fire extinguishers to use are the same as with the CO₂ laser. Flammable
things seem to catch on fire more easily than with the CO₂ laser cutter. There is
a fire sensor that will stop the machine and beep loudly, but the size and length
a flame must be burning before it triggers seems to vary a lot, so you do need to
actively watch what it is doing and have a water spray bottle ready.

### Ventilation

There is a HEPA filter connected to the exhaust port of the machine. It must be on
and set to a high enough speed to clear smoke from the machine into the filter,
with the exhaust exiting outside.

![HEPA filter connected to the machine exhaust](assets/tools/xtool-f1-ultra/img02.jpg)
![Hackspace instructions on a red sign on top of the machine](assets/tools/xtool-f1-ultra/img03.jpg)

## Using the machine

The quick start guide is available from xTool and shows how to set up and turn on
the machine:

- [xTool F1 Ultra Quick Start Guide](https://support.xtool.com/article/1353?from=xTool%20F1%20Ultra&url=%2Fproduct%2F33)

The instructions specific to the hackspace are on a red sign stuck to the top of
the machine (pictured above). The sign is a red aluminum business card and was
engraved using the machine.

- [xTool Learning Center](https://support.xtool.com/learning-center) has videos
  showing how to use the software.

xTool has recommended settings for many materials built into the software, and
additional ones on their website. As usual, some experimentation may be required
to get good results with your exact material. The software has a speed & power
test pattern option built in to help find good settings.

## Issues

### Copper is difficult

Copper is particularly difficult to engrave, and the focus needs to be better than
+/-0.5mm to work well. The speed and power also need to be adjusted carefully.

### Printed circuit boards (PCBs)

FR1 and FR2 (phenolic) are safe to cut and can be cut if you are careful. In FR4
(fiberglass epoxy resin) boards, the epoxy may produce harmful fumes like on a
CO₂ laser, and the glass does not cut.

### IR laser focus height

The xTool F1 Ultra has autofocus, and the autofocus usually reliably sets the
height within about +/-0.5mm. However, the actual focus distance for the IR fiber
laser (for metal) occasionally will shift by up to 4mm relative to the autofocus
height. So far this offset has only changed when the machine is moved. When the
offset is 0mm it can engrave copper over a wide area, but when the offset is 4mm
copper will only engrave near the center, even after compensating for the focus
offset. As of 2025-12-21 it was repaired by xTool and shipped back to us. As of
2026-02, Kurt reported that adjustments were needed after using autofocus.

### Laser isn't found / reconnect by WIFI or USB

Sometimes the software needs to be reconnected to the laser at startup. Follow the
directions from xTool to connect. They keep changing the user interface for it,
but there's usually a find or connect-to-device button somewhere; then select
WIFI and press scan. It should show up in the results, and then you select it
there. Alternatively the machine can be used with a USB cable.

As of 2026-02-07 there is a long USB extension cable going from the computer on
the large CO₂ laser cutter to the xTool F1. The USB cable has a magnetic connector
to the side of the xTool F1 to avoid damage to the laser if the cable gets pulled
on, or the laser is moved. If the USB connection isn't working, check whether the
magnetic connector is fully connected.

### The vent tube disconnects from the back of the machine

There are two parts: a coupler and the spiral tube. The coupler threads onto the
end of the tube by turning the coupler counterclockwise if you are looking through
the coupler at the end of the tube. The coupler has teeth to engage the spiral and
stops, so it will feel tight when it is tightened fully. The larger end of the
coupler connects to the spiral tube, and the smaller end attaches to the back of
the xTool laser.

## LightBurn

LightBurn is now compatible with the F1 Ultra, but we haven't tried it. The F1
Ultra has a lot of specialized modes that aren't available in LightBurn.

## Training

Read this guide and the linked information, and ask any questions that you have.
Ed is usually at project night for questions and for the test to finish training.

Before using the laser, users must read and understand the official safety
training and this guide. The test covers:

- Under what operating conditions the xTool F1 Ultra is a class 4 laser device,
  and what safety precautions would be required to operate it safely under those
  conditions.
- Under what conditions the xTool F1 Ultra can meet the requirements of a class 1
  (or 2) laser device, and what safety precautions are required to operate it
  safely.
- What conditions we operate the laser under, and why this is important.
- What materials are safe and what materials are dangerous.
- Fire safety: have a water spray bottle ready; turn on the air filter and make
  sure the fan speed is on high.
- Turning on the laser (key).
- Operating the machine: focus, update the camera image, make a speed/power test
  pattern, and engrave something.
- Turning off the machine (key).
