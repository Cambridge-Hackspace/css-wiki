# Laser Alignment Guide

## Overview

Guide for aligning the mirrors on the CO₂ laser engraver.

- Model: XM-1060, Series No: HL6953816

If the laser cutter is having issues cutting through material that it has
previously cut without a problem, the mirror alignment has likely drifted out of
alignment due to temperature changes or machine vibrations on the gantry or
cutting head. This guide walks through checking and correcting that alignment.

## Safety

- Setting the pulse power too high can melt the alignment jig and catch the paper
  target on fire. Keep the max power at the recommended low setting (15%) while
  aligning.
- Always close the cover before pressing **Pulse**.
- Alignment of mirror 1 and the tube can be very time-consuming and may require
  re-aligning the cutting head position and mirror 3. Do not attempt mirror 1
  alignment without help, or unless you have experience doing a full alignment.

## Step 1 — Set up pulse mode

Confirm the laser pulse mode is set to a reasonable output to burn paper test
targets using the **Pulse** button on the control panel. If it is set too high it
can melt the jig and catch the paper target on fire.

1. Press the **Z/U** button, and using the arrow buttons select the "Laser Set"
   option from the menu.
2. Confirm the setting is MANUAL. If it's set to "Continue", change it to
   "Manual".
3. Set the output time to 50ms.

   ![Laser Set menu on the control panel](assets/tools/laser-cutter/align-img02.png)

4. Press **Esc** out of this menu and back to the Main Menu.
5. Press the **Max Power** button on the control panel, and set the max power to
   15% if it's not currently at this level.

We now have a way to burn targets easily and consistently with a single press of
the **Pulse** button.

Check the contents of the alignment box and make sure you have enough targets and
that the jigs for calibration are present. Contents should include:

1. Enough paper targets to align the mirrors. Each mirror takes between 5 and 10
   to adjust.
2. Two target holders for mirror 1 and mirror 2.
3. A target holder for the lens / final mirror 3 adjustments.
4. If you run out, you can cut more targets on the smaller laser cutter, or on the
   large cutter assuming it's functional enough to complete this.
5. An SD card containing the files for the jigs and the paper targets.

![Alignment box contents](assets/tools/laser-cutter/align-img03.jpg)

## Step 2 — Alignment check

1. Place mirror 2's jig over the mirror and insert a paper target. Move the
   mirror all the way to the bottom left corner.
2. Close the cover, press **Pulse**, and check that there is a mark dark enough to
   see.
3. Repeat if there is no visible mark, or press Pulse twice at a one-second
   interval.
4. Once you have a clearly visible mark, move the mirror all the way to the top
   left and press Pulse using the same method to verify the new burn mark.
5. Compare this target to the reference target taped to the machine. If it's not
   close then the machine will need a full alignment.
6. If it looks good, move on to Step 3.

![Mirror 2 alignment check target](assets/tools/laser-cutter/align-img04.png)

The burn should be just below the center. This position is aligned to enter mirror
3 dead center. Don't try to correct it.

## Step 3 — Mirror 2 (the "problem child")

This mirror has a tendency to get out of alignment relatively quickly due to the
mirror mount design and vibration from the cutting head movement.

1. Remove the jig on mirror 2 and place the jig for mirror 3 in the cutting head
   mirror hole, and insert a paper target.
2. Move the cutting head half way between the bottom and top of the table, then
   move the cutting head (mirror 3) all the way to the right edge of the table.
3. Close the lid and press **Pulse** until you see a mark on the target.
4. Move the cutting head all the way to the left, closest to mirror 2.
5. Create another mark using the Pulse button. With a perfectly aligned mirror,
   there should be just a single burn dot.
6. If there are two separate dots, go to the mirror 1 alignment section and then
   return to step 7.
7. If it looks good, move the head to the top right-hand corner and do another
   pulse until you see the new mark.
8. If the upper burn mark is on top of the previous burns, move the head to the
   bottom right and do another pulse burn. This one will likely be below and to
   the right a bit. This is normal for this machine.

![Mirror 2 alignment target](assets/tools/laser-cutter/align-img05.png)

## Mirror 1 alignment

Alignment of mirror 1 and the tube can be very time-consuming and may result in
needing to align the cutting head position and mirror 3. Do not attempt this
without help, or unless you have experience doing a full alignment.

1. To do a proper alignment you need to start with the mirror in the back —
   mirror 1, the first mirror the laser hits.
2. You will need a second person to help move the laser cutter away from the wall.
3. This mirror should only be adjusted if the burn dot in the lower-left position
   is off from the burn dot in the upper-left position.
4. Adjusting this mirror should only be done by a member with experience adjusting
   the tube and this mirror.

## Advanced troubleshooting

### Diagnosing laser health using paper targets

If the laser cutter is having issues cutting through material that it has
previously cut without a problem, the mirror alignment has likely drifted out of
alignment due to temperature changes or machine vibrations on the gantry or
cutting head.

What to check:

- **Is the laser cut wider in the horizontal vs the vertical direction?** If yes,
  it can be one of a few things:
  - Mirror 3 on the cutting head is out of alignment and either clipping the lens
    holder, or clipping the air nozzle opening; or
  - Mirror 2 is so far out of alignment that it's clipping the entrance opening to
    mirror 3.
- **Is the cut line fatter than normal?** Verify the nozzle distance to the
  cutting surface is correct; if that is correct, then check the alignment of
  mirror 1.
