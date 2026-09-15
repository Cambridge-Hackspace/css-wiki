# CO₂ Laser Cutter Guide

![CO₂ laser cutter](assets/tools/laser-cutter/img01.png)

## Overview

A laser cutter is a machine that uses a concentrated beam of light (a laser) to
cut or engrave materials like wood, acrylic and cardboard.

This guide is the full reference for the Cambridge Hackspace CO₂ laser cutter,
covering the pre-training reading (safety and machine basics) as well as
intermediate operation, troubleshooting, and maintenance.

For the step-by-step checklist to run before and during a cut, see
[Using the laser cutter](TOOLS/LASERS/USING.md). For material settings and
the section index, see [the Laser Cutter index](TOOLS/LASERS/INDEX.md). The
separate desktop fiber/diode laser is documented at
[xTool F1 Ultra](TOOLS/LASERS/xtool-f1-ultra.md).

### Training overview

To use the CO₂ laser cutter independently, all hackspace members must first
complete in-person training.

1. **Register for training:** Laser training occurs on the 3rd Monday of each
   month from 7:00pm to 8:00pm. To register, fill out
   [this form](https://docs.google.com/forms/d/e/1FAIpQLScMJ4orS5NHJttHPuSDHW1-YVE52wOkWFQ3GWEbLCiZr3yBQg/viewform?usp=publish-editor).
2. **Before training:** Read this guide (especially the [Safety](#safety)
   section) beforehand. It covers safety and machine basics so that in-person
   time can focus on a hands-on demonstration with a mini project. You don't need
   to memorize the text; it's just so everyone arrives with the same baseline
   knowledge, including total beginners.
3. **During training:** In-person training reviews essential safety and includes
   a hands-on project where you'll create a small plywood keychain.
4. **After training:** The [Intermediate laser cutting](#intermediate-laser-cutting)
   section contains additional resources for developing your laser-cutting skills
   beyond the basics.

### What is a laser cutter?

Any project you want to laser cut starts as a **vector file**, like an SVG or
DXF. You upload that file into the laser cutter's software, and the machine
follows the lines in the design to cut or engrave it.

A vector graphic and the cut it produced:

![A vector graphic](assets/tools/laser-cutter/img02.png)
![The resulting cut](assets/tools/laser-cutter/img03.png)

- **Laser beam:** Basically a super strong flashlight that can focus its light
  into a tiny, intense point. This is the laser.
- **Cutting:** When the laser beam hits a material, it generates heat that melts
  the material along the path of the beam, resulting in a cut.
- **Engraving:** By lowering the laser's power or shortening its exposure time,
  only the surface layer is removed. This causes the material to be engraved
  rather than cut through.
- **Precision:** Because the laser is so focused, it can make very detailed and
  precise cuts, much better than a regular saw.
- **Control:** The machine is controlled by a computer, which tells it exactly
  where to cut, allowing for intricate designs.

### What can you make with a laser cutter?

The following projects were made by members of the Cambridge Hackspace.

Engraving on plywood:

![Engraving on plywood](assets/tools/laser-cutter/img04.png)

Engraving on acrylic:

![Engraving on acrylic](assets/tools/laser-cutter/img05.png)

The "*Nerdy Gurdy*" is a playable, laser-cut instrument (more info:
<https://www.nerdygurdy.nl/>):

![The Nerdy Gurdy laser-cut instrument](assets/tools/laser-cutter/img06.png)

Cutting foam into 2D shapes that are assembled into a 3D object:

![Foam cut into 2D shapes assembled into a 3D object](assets/tools/laser-cutter/img07.png)

Make custom boxes. [This article](https://makerdesignlab.com/tutorials-tips/online-file-generators-for-laser-cutting/)
contains a compilation of popular vector design generators for boxes, puzzles,
gears, and mazes:

![Custom laser-cut boxes](assets/tools/laser-cutter/img08.png)

You can create basically anything by using a vector graphics editor. Laser
cutters use vector files, which have `.svg` and `.dxf` file extensions. We
recommend [Inkscape](https://en.wikipedia.org/wiki/Inkscape) and
[Onshape](https://www.onshape.com/en/) as free vector editors.

### Machine specifications

- Our laser cutter model is the "large 100W CO₂ HL-Laser XM-1060".
- The maximum cutting area is 100cm x 60cm.
- The cut width is around 0.15mm, but this can vary with speed and material.
- All hackspace members incur a cost of $0.50/minute of cutting time. Cutting
  time only increases when the laser is actively firing. If you think you will be
  using the machine a ton, we do offer a rate of $0.35/minute if you pre-pay
  $100. These fees cover the cost of replacement parts for the machine and air
  filters.

### Parts of the machine

The mirrors move so the beam travels from the laser tube to mirror 1, then along
the Y axis to mirror 2, and then along the X axis to mirror 3, and then down to
the lens with the light focused about 10mm below the end of the nozzle.

The laser tube is inside the top back compartment which is kept locked for
safety.

## Safety

The operator must stay near the machine and pay attention to it **at all times**
in case there is a fire. Even if your cut has a long duration (like 45 minutes),
you must remain **nearby** and check on the laser every couple of minutes.

Small fires can be extinguished easily with a water spray bottle, but can quickly
grow large if the operator isn't paying attention.

### NEVER cut these materials

You MUST know what your material is made of before cutting anything! Some
materials can produce **toxic fumes** when heated by the laser.

Our list of materials is based on
<https://wiki.asmbly.org/index.php?title=Laser_Cutter_Materials> with a few
changes (the ~~strikethrough~~ items).

**WARNING:** Because many plastics are dangerous to cut, it is important to know
what kind you are planning to use. The website *Make* has a How-To for
identifying unknown plastics with
[a simple process](https://makezine.com/2011/09/22/identifying-unknown-plastics/).

| Material | DANGER! | Cause/Consequence |
| --- | --- | --- |
| PVC (Poly Vinyl Chloride)/vinyl/pleather/artificial leather | Emits chlorine gas when cut! | Don't ever cut this material as it will ruin the optics, cause the metal of the machine to corrode as chlorine is released, and ruin the motion control system. |
| Polycarbonate/Lexan | Cuts very poorly, discolors, catches fire | Polycarbonate is often found as flat sheet material. The window of the laser cutter is made of Polycarbonate because *polycarbonate strongly absorbs infrared radiation!* This is the frequency of light the laser cutter uses to cut materials, so it is very ineffective at cutting polycarbonate. Polycarbonate is a poor choice for laser cutting. It creates long stringy clouds of soot that float up, ruin the optics and mess up the machine. |
| ABS | Melts / Cyanide | ABS does not cut well in a laser cutter. It tends to melt rather than vaporize, and has a higher chance of catching on fire and leaving behind melted gooey deposits on the vector cutting grid. It also does not engrave well (again, tends to melt). Cutting ABS plastic emits hydrogen cyanide, which is unsafe at any concentration. |
| HDPE/milk bottle plastic | Catches fire and melts | It melts. It gets gooey. It catches fire. Don't use it. |
| PolyStyrene Foam | Catches fire | It catches fire quickly, burns rapidly, it melts, and only thin pieces are cut. This is the #1 material that causes laser fires! |
| PolyPropylene Foam | Catches fire | Like PolyStyrene, it melts, catches fire, and the melted drops continue to burn and turn into rock-hard drips and pebbles. |
| Epoxy | Burn / smoke | Epoxy is an aliphatic resin, strongly cross-linked carbon chains. A CO₂ laser can't cut it, and the resulting burned mess creates toxic fumes (like cyanide!). Items coated in Epoxy, or cast Epoxy resins, must not be used in the laser cutter. (See Fiberglass.) |
| Fiberglass | Emits fumes | It's a mix of two materials that can't be cut: glass (etch, no cut) and epoxy resin (fumes). |
| Coated Carbon Fiber | Emits noxious fumes | A mix of two materials. Thin carbon fiber mat can be cut, with some fraying — but not when coated. |
| Any foodstuff (meat, seaweed 'nori' sheets, cookie dough, bread, tortillas…) | The laser is not designed to cut food, and people cut things that create poisonous/noxious substances such as wood smoke and acrylic smoke. | If you want to cut foodstuffs, consider sponsoring a food-only laser cutter for the space that is kept as clean as a commercial kitchen would require. |
| Material with sticky glue backing | Coats lens, cracks lens | There are many normally laserable items such as thin wood laminates that you can purchase that become un-cuttable when the manufacturer adds a layer of peel-off glue on the bottom to attach them to surfaces. Examples include cork tiles, thin wood laminate, acrylic tiles, and paper stickers. Never cut these materials in the laser cutter if they have this backing. The glue will vaporize forming a coating on the lens that will coat it, cloud it, heat it, and then potentially crack the lens. The glue residue is worse than resin, and can't be removed without risking damage to the lens, requiring a lens replacement. |
| Nylon | Emits fumes | Hydrogen cyanide gas (HCN). |
| ANY metals | Damages the machine | Metals can reflect the CO₂ laser and may damage the lens. Instead, many metals can be cut using our [xTool fiber laser](TOOLS/LASERS/xtool-f1-ultra.md). |

### Safe materials for cutting

| Material | Max thickness | Notes | WARNINGS! |
| --- | --- | --- | --- |
| Many woods | 1/4" | Avoid oily/resinous woods. | Be very careful about cutting oily woods, or very resinous woods, as they also may catch fire. |
| Plywood/Composite woods | 1/4" | These contain glue, and may not be laser cut as well as solid wood. |  |
| MDF/Engineered woods | 1/4" | These are okay to use but may experience a higher amount of charring when cut. |  |
| Paper, card stock | thin | Cuts very well on the laser cutter, and also very quickly. | Can quickly catch fire. |
| Cardboard, carton | thicker | Cuts well but may catch fire. | Watch for fire. |
| Cork | 1/8" | Thin cork can be cut, but the quality of the cut depends on the thickness and quality of the cork. Engineered cork has a lot of glue in it, and may not cut as well. | Avoid cutting thicker cork (5mm). Engraves well, cuts poorly. |
| Acrylic/Lucite/Plexiglas/PMMA | 1/2" | Cuts extremely well leaving a beautifully polished edge. |  |
| ~~Thin Polycarbonate Sheeting (<1mm)~~ (only special low-chlorine polycarbonate) | <1mm | Very thin polycarbonate can be cut, but tends to discolor badly. Extremely thin sheets (0.5mm and less) may be cut with yellowed/discolored edges. Polycarbonate absorbs IR strongly, and is a poor material to use in the laser cutter. | Watch for smoking/burning. |
| Delrin (POM) | thin | Delrin comes in a number of shore strengths (hardness) and the harder Delrin tends to work better. Great for gears! |  |
| Kapton tape (Polyimide) | 1/16" | Works well, in thin sheets and strips like tape. |  |
| Mylar | 1/16" | Works well if it's thin. Thick mylar has a tendency to warp, bubble, and curl. | Gold coated mylar will not work. |
| Solid Styrene | 1/16" | Smokes a lot when cut, but can be cut. | Keep it thin. |
| Depron foam | 1/4" | Used a lot for hobbies, RC aircraft, architectural models, and toys. 1/4" cuts nicely, with a smooth edge. | Must be constantly monitored. |
| Gator foam |  | Foam core gets burned and eaten away compared to the top and bottom hard paper shell. | Not a fantastic thing to cut, but it can be cut if watched. |
| Cloth/felt/hemp/cotton |  | They all cut well. Our lasers can be used in lace-making. | Not plastic coated or impregnated cloth! |
| Leather/Suede | 1/8" | Leather is very hard to cut, but can be if it's thinner than a belt (call it 1/8"). Our "Advanced" laser training class covers this. | Real leather only! Not 'pleather' or other imitations — they are made of PVC. |
| Magnetic Sheet |  | Cuts beautifully. |  |
| NON-CHLORINE-containing rubber (Silicone, polyisoprene) |  | Fine for cutting. | Beware chlorine-containing rubber! |
| ~~Teflon (PTFE)~~ We don't cut fluorinated plastics | thin | Cuts OK in thin sheets. See <https://www.ulsinc.com/materials/teflon>; the issues listed in <https://en.wikipedia.org/wiki/Polymer_fume_fever> should not matter because our lasers are fully vented and exhausted. |  |
| Carbon fiber mats/weave that has not had epoxy applied |  | Can be cut, very slowly. | You must not cut carbon fiber that has been coated! |
| Ethylene-Vinyl Acetate (EVA) Foam |  | OK to cut. | This material does not support a channel, so even though thin pieces cut super easy, that doesn't scale the same way for thicker pieces. |
| Coroplast ('corrugated plastic') — make sure it is Polypropylene | 1/4" | Difficult because of the vertical strips. Three passes at 80% power, 7% speed, and it will be slightly connected still at the bottom from the vertical strips. |  |
| Polyester |  | OK according to <https://support.epiloglaser.com/laser-machine/fibermark/faq/material-safety-and-your-laser/> (the MSDS doesn't list any dangerous combustion products). | See if you can get an MSDS for your material. |

### Safe materials for etching

All the above "cuttable" materials can be etched, in some cases very deeply. In
addition, you can etch:

| Material | Notes | WARNINGS! |
| --- | --- | --- |
| Glass | Green seems to work best; looks sandblasted. | Flat glass should be engraved in our cutter as we have no rotary device. Round or cylindrical objects like bottles or glasses will have distortion. |
| Ceramic tile |  |  |
| Anodized aluminum | Vaporizes the anodization away. |  |
| Painted/coated metals | Vaporizes the paint away. | Make sure the paint is safe to laser (like water-based acrylic). |
| Stone, Marble, Granite, Soapstone, Onyx | Gets a white "textured" look when etched. | 100% power, 50% speed or less works well for etching. |

### Electrical safety

The laser tube operates at around 25,000 volts (25KV). Do not open the locked
panels of the machine on the back (laser tube area), or right side (electronics),
unless you understand the risks and know how to work with high voltage
electronics safely.

### If a fire happens

![Fire response](assets/tools/laser-cutter/img13.png)

1. Push the **emergency stop button** below the laser's control panel.
2. Only open the lid **after** pushing the stop button to avoid damaging your
   eyes from the laser.
3. For small (birthday-candle sized) fires, use the water spray bottle.
4. If you're always watching the laser, you **likely won't** see a medium or
   large fire.
5. For medium and large fires, follow this protocol: EZ fire spray ➔ the fire
   blanket ➔ fire extinguisher ➔ call 911 and evacuate.

The following are located to the left of the CO₂ laser cutter:

![Fire extinguishers located to the left of the laser cutter](assets/tools/laser-cutter/img14.png)

- **Fire extinguisher 1 — Water spray bottle.** Good for the small
  (birthday-candle sized) fires that we have had in the past.
- **Fire extinguisher 2 — EZ Fire Spray.** Good for barbeque-sized fires and
  works like a regular spray can (like spray-paint or cooking spray) where you
  remove the lid and press on the top to spray it. It won't damage the machine,
  so definitely try it if the water spray bottle isn't enough.
- **Fire extinguisher 3 — Fire blanket.** There are fire blankets behind the
  wall-mounted fire extinguishers in red pouches. Grab the black straps dangling
  from the pouch to deploy the blanket. It's a fiberglass blanket which is very
  fire-resistant, so draping it over the laser cutter should smother a fire.
- **Fire extinguisher 4 — ABC dry chemical fire extinguisher.** Good for larger
  fires, but the dry chemical leaves an acidic residue when it mixes with
  moisture from the air. This may destroy electronics like the computer and the
  electronics in the laser cutter, so it should be used to prevent the building
  from burning down if the above options fail.

## Training goals

After reading the above, you should understand the following:

1. Always watch the laser while it is cutting or etching.
2. Before lasering ANY material, check whether it falls in our
   [safe materials list](#safe-materials-for-cutting) or the
   [dangerous materials list](#never-cut-these-materials).
3. If you don't know what a material is, you CANNOT cut or engrave it.
4. Some examples of safe materials are: cardboard, paper, plywood, acrylic.
5. Some examples of dangerous materials are: Polycarbonate, ABS, PVC, Nylon.
6. The fire escalation protocol is: emergency stop button ➔ open the lid ➔ water
   spray bottle ➔ EZ fire spray ➔ fire blanket ➔ fire extinguisher ➔ call 911.
7. All hackspace members incur a cost of $0.50/minute of cutting time, or
   $0.35/minute if you pre-pay $100.

After completing in-person laser training, you will be able to:

**Operate the machine**

- Focus the laser with the stair-step focus stick without damaging the nozzle.
- Use the control panel to move the laser nozzle and adjust the bed height.

**LightBurn basics**

- Import a vector file.
- Add shapes and text.
- Assign layers to each vector.
- Distinguish between Cut and Engrave (Line and Fill).
- Set speed, power, and number of passes.
- Use the LightBurn power/speed material test pattern.
- Use the laser's camera to align cuts on material accurately.
- Understand the difference between "Absolute Coords" and "User Origin."
- Use "Cut Selected Graphics" and "Use Selection Origin."
- Frame a job before cutting to confirm position.
- Preview a job safely before running it.
- Successfully laser-cut a keychain from plywood!
- Receive an RFID card that grants access to the laser through Toolpass.
  Non-members will NOT receive one of these.
- Perform basic laser machine maintenance of the mirrors with isopropyl alcohol.

## Intermediate laser cutting

Additional resources for developing your laser-cutting skills beyond the basics.
For the pre-cutting and cutting checklist, see
[Using the laser cutter](TOOLS/LASERS/USING.md).

### Move the laser nozzle

![Control panel main menu](assets/tools/laser-cutter/img15.png)

- When the main menu is visible, use the arrow buttons to move the nozzle in any
  cardinal direction.
- Once you are happy with the nozzle position, press the **Origin** button to set
  this location as the starting point for your cut.

### Adjust the bed height

![Adjusting the bed height on the control panel](assets/tools/laser-cutter/img16.png)

- Press the **Z/U** button.
- While on the Z/U screen, press the **left arrow** to raise the bed.
- Press the **right arrow** to lower the bed.
- Adjust the bed height until the arrow on the stair-step focus tool aligns
  between your material and the nozzle. *Please* remove the step tool while moving
  the bed.
- Press **Esc** to save this bed position.

### What are speed and power?

Cuts on wood are normally performed at 100% power, where the speed is adjusted as
needed. A speed of 30mm/s is a good starting point for materials that are less
than 6mm thick. If you want to make sure that everything is cut through fully then
setting the minimum power to 100% works well, but it can burn the corners more as
it slows down. To avoid burning corners the "minimum power" setting could usually
be lower, like at 15%; this allows the power to be reduced when the speed is lower
(e.g., during acceleration and deceleration for ends and corners), but not
reduced so much that the laser turns off.

Engraving can be 10%–100% power at a speed of 100–400mm/s (usually). Somewhere
around 600mm/s or faster the motors may lose the position. Higher speeds need
space for acceleration and will reduce the cutting area.

- Note: The laser does not turn on unless the power >= 10%.
- Engrave with X-axis movement (it's faster and shakes the machine less).
- Tip: Before cutting or engraving your full design, perform a small test on your
  material to confirm whether the settings yield your desired look. You can use
  LightBurn to create a small square to test cutting or sample text to test
  engraving. This way, you can test varying power/speed without wasting much
  material.

### Power vs power %

The laser tube turns on at about 10%, increases quickly to about 20%, increases
more slowly up to 80%, and then is about the same up to 100%. In other words, the
relationship between the power % setting and the actual output power is not
linear.

### How to use LightBurn

- LightBurn documentation: <https://docs.lightburnsoftware.com/latest/>
- User interface: <https://docs.lightburnsoftware.com/latest/GetStarted/UITour/>
- Drawing and importing files: <https://docs.lightburnsoftware.com/latest/GetStarted/CreatingAndImportingArtwork/#importing>

#### Connecting LightBurn to the laser if you are running it on your own computer

- Make sure you are connected to the Hackspace wifi or ethernet.
- When adding a new laser, LightBurn considers it a "DSP" laser using a "Ruida"
  controller. The controller's IP address is taped to the machine (ask a
  trainer if you can't find it).
- Our laser has the back left corner as the origin.
- The cutting area is 1000x600mm.
- LightBurn has more information here:
  <https://docs.lightburnsoftware.com/latest/GetStarted/FindMyLaser/>

#### Troubleshooting connecting to the laser cutter

- Make sure that it says "Lan ON" in the lower right corner of the laser cutter
  screen. This means that it is connected to the network, and if this is off it
  isn't going to work. There might be a cable disconnected somewhere, or the
  laser or your computer might need to be restarted.
- Check if LightBurn says it is connected to the laser cutter.
- The laser works best when connecting by WIFI or Ethernet, or USB drive. It has
  a USB cable which can be used directly but it is slower so we don't use it. The
  computer at the laser cutter might still have both USB and Ethernet IP
  connections in case one isn't working and can get switched to the other one
  occasionally.
- Make sure you are on the Hackspace WIFI (chack-2.4 or chack-5) and not Comcast
  or something else.
- Turn it off and on again. Both the laser and computer.
- Try posting on the Discord or ask at project night.
- Use a USB drive to move your file to the laser from LightBurn:
  - LightBurn can save output to a file on a USB drive.
  - The laser cutter can read the USB stick if it's plugged into the correct port
    on the laser cutter.
  - The other port is for the USB cable to the computer.

#### LightBurn power/speed test pattern

To find the settings that work well for a material there is a material test:
<https://docs.lightburnsoftware.com/latest/Reference/MaterialTest/>

![Example LightBurn material test grid](assets/tools/laser-cutter/img20.png)

An example test grid from the LightBurn documentation showing an engraving test
varying the speed and power %. The power/speed for cutting can also be tested.

If the squares are too small the laser cutter won't have time to accelerate to
full speed, so if you are testing faster cutting make the squares larger than the
default.

#### LightBurn focus test

The focus test moves the bed down, so start with the nozzle closer to the
material than the normal focus distance. After the test, pick the best (usually
the thinnest line) offset and move the bed down in Z by that distance using the
move control in LightBurn.

<https://docs.lightburnsoftware.com/latest/Reference/FocusTest/>

![Example LightBurn focus test](assets/tools/laser-cutter/img21.png)

An example focus test from the LightBurn documentation.

## Troubleshooting common problems

### If the Toolpass isn't working or is off

Unplug the Toolpass for a moment. The Toolpass extension cord is plugged into the
outlet behind the laser cutter and will have an engraved tag labeled "Laser" tied
to it near the plug. The tag may be turned sideways and hard to see. The laser
cutter Toolpass plug must be plugged directly into the wall socket and not into a
power strip.

### If the cut looks unusual, like if horizontal and vertical cuts are different widths

Clean the mirrors and lens (see the next section).

De-focus the laser by moving the bed down (maybe 100mm or more) and check if it
is a nice circle. If it makes a different shape the beam may be hitting the edge
of a mirror or the nozzle and will need alignment. See
[Laser alignment guide](TOOLS/LASERS/ALIGNMENT.md).

### If the laser won't shoot at all

- Check if the lid switch is working. The lid needs to be closed and pressing the
  switch for the laser to turn on.
- There is a switch on the front of the machine below the display that turns off
  the laser (the black switch on the right).

  ![Black laser-enable switch below the display](assets/tools/laser-cutter/img22.jpg)

- Check if the water protect light is on (usually an orange LED on the laser power
  supply labeled P). Checking it requires opening the side panel of the machine
  and should only be done by people who understand the risks of high voltages and
  know how to do so safely. If this light is off then the laser won't fire. We had
  the water flow sensor fail on one of the laser cutters where the magnetic switch
  on the side of the flow sensor had loose screws and needed to be adjusted and
  tightened. The water protection should be 0v when the LED is on if the power
  supply doesn't have a water-protected LED.

### If the circuit breaker trips

Stop and figure out what is on the same circuit. This should not happen and you
should not turn the circuit breaker back on until power has been balanced between
circuits properly. We have had problems and moved the 3D printers and microwave
to their own circuit. One air conditioner is currently on the same circuit and
the outlet and plug are labeled — the air conditioner is set up to turn off
automatically when the laser cutter is used.

### "Frame slop" error

This means the engraving is too close to the side of the laser cutter bed. The
machine needs room to speed up to get to the engraving speed. Move the engraving
away from the side of the bed.

## Cleaning and replacing parts

The mirrors and lens should be cleaned after several hours of operation, or more
often if there is a lot of smoke. A small amount of smoke sticking to the mirrors
is normal. If too much soot accumulates the mirror (or lens) will start to heat up
and bake on the dirt and destroy the mirror (or lens).

### Cleaning mirrors

Use a cotton swab (Q-tip) wrapped with a lens cleaning wipe (Zeiss glasses
cleaning wipe). Clean in a spiral growing from the inside to the outside and
repeat with a clean part of the wipe until it is clean. See the mirror path
described in [Parts of the machine](#parts-of-the-machine) for mirror 1, 2, and 3
locations.

### Cleaning the lens

Use a lens cleaning wipe (Zeiss glasses cleaning wipe). The lens is made from zinc
selenide and should not be touched. Use nitrile gloves and avoid skin contact
with the lens.

### How to get to the lens

The lens is inside the tube/nozzle below the 3rd mirror. It's kind of hard to get
to and usually the air tube to the nozzle needs to be disconnected. Make sure the
air tube is re-connected before cutting anything.

### Replacing mirrors

Mirrors can be ordered online. The machine uses 25mm mirrors (double-check this).

### Replacing the lens

Disconnect the air tube by pushing on the blue push-to-connect fitting while
pulling out the air tube. When the push-to-connect fitting is pressed right the
tube should be very easy to remove.

Un-screw the lower half of the nozzle. There are two sections of the nozzle and
the upper one has a ring that you can hold to make it easier to unscrew the lower
half.

Inside the nozzle the lens is held in place by a ring that uses a pin spanner to
turn it. Snap ring pliers will also work.

Check if the lens is dirty and clean it with a lens cleaning wipe (Zeiss wipe).

![Snap ring pliers in the holes to unscrew the retaining ring](assets/tools/laser-cutter/img24.jpg)

![A dirty lens with a cloudy center area](assets/tools/laser-cutter/img25.jpg)

Above: the cloudy center area is very dirty. After cleaning, the lens is very
reflective and the posters on the wall are visible.

## Replacing air filters

The exhaust runs through a pre-filter, HEPA filters, and a carbon filter, which
are replaced as they load up.

## Replacing the CO₂ laser tube

The laser tube is big, heavy, and made of glass. It's also filled with water and
has wires connected to it that can be at around 25,000V when the machine is on.
Please be careful and take appropriate safety precautions, and make sure the
voltage is safely discharged before touching it. Don't open the electrical access
panels unless you understand the risks.
