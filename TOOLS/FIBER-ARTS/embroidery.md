# CNC Embroidery Machine (Brother SE700)

## Overview

A CNC embroidery machine automates embroidery by translating a vector design into instructions that guide how its motorized needle stitches your fabric. The Hackspace machine is a Brother SE700.

Unlike the 3D printers, wood shop, and laser cutters, the CNC embroidery machine does **not** require in-person training prior to use. If you would like to use this machine, simply read [Section 1: Embroidery Basics](#section-1-embroidery-basics) below to get started.

However, if you would prefer live instruction, we also have optional in-person training for the embroidery machine from 7:00pm - 8:00pm on the first Monday of each month. To register, fill out this form: <https://forms.gle/QLveb9GHWeA79R1EA>.

If you have any questions, feel free to drop them in our Discord ([click here to join](https://discord.gg/WnFK8sQaGD)).

---

## Section 1: Embroidery Basics

### What is a CNC embroidery machine?

A CNC embroidery machine automates embroidery by translating a vector design into instructions that guide how its motorized needle stitches your fabric.

### Examples of CNC embroidery at Hackspace

This bee is one of many designs that came pre-loaded with the Brother SE700.

![Bee design embroidered on fabric](assets/tools/embroidery/img02.png)

This Eastern Tiger Swallowtail was designed in Inkscape. The first image is the vector graphic that was sent to the embroidery machine. The [Inkscape section](#section-2-using-and-understanding-inkscape) contains instructions for creating your own patches from any image.

![Swallowtail vector design in Inkscape](assets/tools/embroidery/img03.png)
![Finished swallowtail embroidered patch](assets/tools/embroidery/img04.png)

### Watch this video first

It demonstrates the basics by embroidering a pattern onto a sweater: <https://www.youtube.com/watch?v=mKNbj3NcE_o&t=315s>

The pattern produced in the video:

![Pattern embroidered onto a sweater](assets/tools/embroidery/img05.png)

### Hackspace thread

The Hackspace supplies a **40 WT thread** that is free to use. For the cleanest look, use the same thread for the bobbin and upper thread.

You can find instructions for filling a bobbin in [Refilling the bobbin](#refilling-the-bobbin).

#### Needle sizes

The needle's eye should be twice the diameter of your thread. That means our 40 WT thread requires a **75/11** or **80/12** embroidery needle.

#### Needle shapes

There are two types of needle shapes, **sharp and ballpoint**:

1. Sharp needles have a pointed tip for woven fabrics.
2. Ballpoints have a rounded tip for knits and fine fabrics.

### Machine usage tutorials

#### Replacing the needle

The extra needles are located in the top drawer of the organizer to the left of where the machine is stored. Tutorial for needle replacement: <https://www.youtube.com/watch?v=i7nnOMOYJG4>

#### Threading the upper thread

Video tutorial: <https://www.youtube.com/watch?v=tWGFSYd2f_8>

#### Refilling the bobbin

Video tutorial: <https://www.youtube.com/watch?v=phflfD_9wUI>

#### Loading fabric and stabilizer into the hoop

Video tutorial: <https://www.youtube.com/watch?v=akxFZS7xsbU>

---

## Section 2: Using and Understanding Inkscape

### Make your own designs with Inkscape and Ink/Stitch

You can create your own embroidery designs and transfer them to the machine via a USB drive. We recommend using Inkscape and Ink/Stitch (both are free and open-source) to make custom embroidery graphics. Inkscape is a vector graphics editor similar to Adobe Illustrator, and Ink/Stitch is an Inkscape extension that converts vector designs into embroidery files that our machine can read.

- **Inkscape download:** <https://inkscape.org/release/inkscape-1.4.2/>
- **Ink/Stitch download:** <https://inkstitch.org/docs/install/>

If you would prefer not to download the software, it is also available on the desktop computer located next to our CO2 laser cutter.

**If the Inkscape extensions folder is missing:** If Ink/Stitch cannot locate the Inkscape extensions folder, install the extension using Inkscape's built-in extensions manager:

1. Click Extensions > Manage Extensions > Install Packages.
2. Installing any extension that supports your Inkscape version will create the extensions folder (for example "Scientific Inkscape" supports Inkscape 1.4).
3. Extensions that are only for older Inkscape versions are listed but will disable the "Install" button.
4. Restart your computer and reopen Inkscape.

### Multi-colored and single-colored embroidery designs

The Brother SE700 embroidery machine supports embroidery with multiple thread colors. It can automatically detect different shades in your design file and separate each color region into its own segment to stitch. Once one unique color's segment has finished stitching, the machine will pause and wait for you to replace the thread spool with the next shade. Once the new color is threaded, you can resume embroidering to begin stitching the next color segment.

![Multi-color design in Inkscape](assets/tools/embroidery/img06.png)
![Color segments separated for stitching](assets/tools/embroidery/img07.png)

### Vectorize image (if needed)

The embroidery machine only accepts vector graphic files. Therefore, raster images (JPEG/PNG) need to be converted into a vector (SVG). If the file you opened is already an SVG (scalable vector graphic) file, you can skip this step.

You can design your vector in another software like Adobe Illustrator first, and then skip to [Configure embroidery settings with Params](#configure-embroidery-settings-with-params).

- Open your design file (JPG, PNG) and use Ctrl+A to select the entire image.
- Navigate to Path > Trace Bitmap > Multicolor (or Single Scan if you only want one thread color) > Colors (detection mode) > Apply.
- Make sure "Stacked" is NOT checked.
- See [Trace Bitmap](#trace-bitmap) for a description of what each Trace Bitmap setting does (highly recommended).
- Each image has a minimum threshold of scans needed to capture all of its desired details. If an element of your image isn't being registered, increase the number of scans.

![Trace Bitmap dialog in Inkscape](assets/tools/embroidery/img08.png)

### View your vector layers

- To view all of your scans (each separated layer): Ctrl + Shift + L.
- The number of generated paths will correspond to the number of scans you requested in the previous step.
- We only want the vector paths, so delete the original image by selecting *image1* and clicking the trash icon.

![Layers panel showing generated paths](assets/tools/embroidery/img09.png)

- You might not need each path that is generated. Toggle the eye icon to show/hide each path and inspect them for unnecessary noise. For example, here are the three paths generated by the previous step:

![Generated path 1](assets/tools/embroidery/img10.png)
![Generated path 2](assets/tools/embroidery/img11.png)
![Generated path 3 with noise](assets/tools/embroidery/img12.png)

- As you can see, *path3* only contains some unintended noise that Trace Bitmap picked up. This noise also overlaps with *path4*, so it should be deleted. The machine automatically pauses for a thread change with each path, so keeping this layer would cause an extra thread-change stop and re-stitch over *path4*.
- If the path names get confusing, you can rename them by right-clicking a layer and selecting the rename option.

### Specify the order your layers will be stitched

The Brother SE700 stitches in the order that layers appear in the *Layers* or *Objects* panel, starting from the bottom and proceeding upward.

For instance, *path4* would be stitched first in the image above. Then, the machine would pause and let you change the thread before stitching *path2*. You can select and drag each path to reorder it.

### Specify the intended dimensions of your design

![Width and height fields in Inkscape](assets/tools/embroidery/img13.png)

- You must specify the exact width and height (in mm) you want your final embroidered design to be. The maximum dimensions of any embroidery design is 100 x 100 mm.
- To adjust the size: Ctrl + A, then set units to mm, and input the width/height (labeled W and H above).

### Configure embroidery settings with Params

- Use the *Params* mode to view a simulation of each colored segment's exact stitch path, see jump stitches, select a stitch/fill method, and configure additional embroidery parameters.
- **Jump stitches** are loose cross stitches that appear when the needle moves from one section of an embroidery design to another. They can be snipped off with scissors or a thread cutter.
- An illustrated description of each fill stitch type can be found here: <https://inkstitch.org/docs/stitch-library/>
- Navigate to Extensions > Ink/Stitch > Params > Apply and Quit.
- Ink/Stitch applies parameter settings only to the currently selected path(s). This means you can select different paths and assign unique stitch types or other parameters to each one.
  - To do this, select the desired path(s) (each of which is a layer), then open the Params menu and configure your desired stitch settings. Click Apply and Quit to save these settings for the selected path(s). If a path is not explicitly configured in the *Params*, it will default to using *auto fill* stitching.

![Ink/Stitch Params simulation](assets/tools/embroidery/img14.png)

### Realistic preview of finished paths

- If you've chosen any fill stitch method other than Auto Fill for a patch, this simulation lets you observe the difference in stitch pattern textures.
- You can simulate your patch's stitch texture by navigating to Extensions > Ink/Stitch > Visualize and export > Stitch Plan Preview > Render mode: Realistic View (high quality).

![Realistic stitch plan preview](assets/tools/embroidery/img15.png)

Example where each path has a different fill type: patch with "Circular Fill" stitch pattern for the gray path (path4) and "Auto Fill" for the black path (path2).

![Patch with mixed fill types](assets/tools/embroidery/img16.png)

### Export vector as an embroidery file (.dst)

- Navigate to: File > Export > Save as Tajima Embroidery Format (.dst).
- Save this file onto a USB drive and then insert it into the Brother SE700 embroidery machine.

![Export as .dst dialog](assets/tools/embroidery/img17.png)

### Finished product

![Finished embroidered patch](assets/tools/embroidery/img18.png)

---

## How to configure a satin stitch

To assign satin stitch to one specific path while other paths use auto fill, leave the other paths untouched (they default to auto fill stitching) or apply different stitch types individually. Ink/Stitch applies settings only to the currently selected path(s). Thus, you can select different path(s) and apply a unique stitch type to each one.

1. Ensure that your design is a vector. If not, see [Trace Bitmap](#trace-bitmap) for steps to trace the bitmap of your raster image.
2. Ensure your selected vector path(s) contain only a fill and no stroke. Open the Fill and Stroke menu (Shift+Ctrl+F). Set a fill color and remove any stroke color (see [Fill and Stroke](#fill-and-stroke) for a demo). The fill object is what Ink/Stitch converts into satin stitches when using "Fill to Satin".
3. Create rungs (short crossing stroke lines) across the fill. These are necessary guides that set the stitch direction. Use the Bezier tool (Ctrl+B) to draw at least two straight lines crossing the filled path from one edge of your shape to the other. The rungs should have a stroke only, no fill (see [Fill and Stroke](#fill-and-stroke) for a demo).
4. Select your rung paths and combine them with Ctrl+K.
5. Select both your original filled path and the rungs path simultaneously by shift-clicking.
6. Go to Extensions > Ink/Stitch > Tools: Satin > Fill to Satin.
7. Adjust options such as starting/ending at a rung or underlays if desired, then click "Apply".

![Fill to Satin tool in Ink/Stitch](assets/tools/embroidery/img19.png)

To preview your design, go to Extensions > Ink/Stitch > Visualize and Export > Simulator.

---

## Trace Bitmap

- **Trace Bitmap** converts raster images (JPEG, PNG) into vector graphics (SVG, DXF, DST).
- Because vector files can be scaled infinitely without losing quality, they are great for laser cutting, engraving, and machine embroidery.
- **Single scan mode** turns a raster image into a single-path trace (black and white only).
- **Multicolor mode** turns a raster image into multiple vector paths (layers) based on a color value delimiter.

![Trace Bitmap mode options](assets/tools/embroidery/img20.png)

### Multicolor mode settings

**Brightness steps:** Splits the image into vector paths based on distinct brightness levels.

**Colors:** Splits the image into vector paths based on distinct color regions.

**Grays:** Splits the image into vector paths based on distinct grayscale values.

**Scans (number):** The number of separate layers (vector paths) created.

- More scans = more detail + complexity.
- Each image has a minimum threshold of scans needed to capture all desired details in the image.
- If an element of your image isn't being registered, increase the number of scans.

**Smooth:** Automatically softens jagged edges in your image.

**Stack (when checked):**

- Each scan (color, brightness, or gray level) is returned as a separate vector path.
- These separate paths are "stacked" (layered) on top of each other, aligned to create the full traced image.
- This prevents gaps or "holes" between layers; each path overlaps with those above it, so the entire area is filled.
- In the layers tab, you can then select any individual vector path to move, recolor, or edit it.

**Stack (when unchecked):**

- This is normally what you want.
- Each scan is also a separate vector path, but the shapes do not overlap to create a filled composite effect.
- Instead, the paths are packed so only the top scan is visible where the shapes overlap; the paths fit like puzzle pieces without any overlap.
- The result is a group of objects, but they are not layered; this can leave gaps or transparency if the scans don't fully cover the whole image.

**Remove Background:** Removes the bottom-most background color.

**Speckles:** Defines the minimum size (in pixels) of disconnected shapes or noise that will be removed during the trace. For example, if set to 5 pixels, all disconnected shapes or noise smaller than 5 pixels wide or tall will be removed. Spots that are 5 pixels or larger will be converted into a trace.

**Smooth corners:** Rounds sharp corners. 0 = sharp angles preserved, larger number = rounded look.

**To view all of your scans (each separated layer):**

- Press Ctrl + Shift + L.
- The number of paths will correspond to the number of scans you requested.
- Now you can select a path to freely move or edit it.

![Scans shown as separate layers](assets/tools/embroidery/img21.png)

---

## Fill and Stroke

- **Fill and stroke** are the two fundamental components of a vector.
- **Fill** is the color inside a vector shape (area).
- **Stroke** is the outline of the shape (perimeter).
- Together, they control how a vector object looks.

*Figure 1* - Original vector path:

![Original vector path](assets/tools/embroidery/img22.png)

*Figure 2* - Vector path after the fill was recolored to blue, the stroke was recolored to red, and the stroke width was increased from 0.5px to 3px:

![Vector path with recolored fill and stroke](assets/tools/embroidery/img23.png)

### How fill and stroke affect embroidery design

- Embroidery machines use the vector objects and their paths for stitching.
- "Fill" defines what area gets filled with stitches, while "stroke" defines stitch paths and borders.
- Clear strokes and solid fills help produce cleaner embroidery patterns.
- If you would like to add a border around a vector path, you can increase the path's stroke width.
- Gradients and complex fills have no effect on stitching; only the vector shapes matter.

### Fill tab

- Open with Shift + Ctrl + F or via the menu: Object > Fill and Stroke.
- This tab controls whether the interior of your selected shape has a color filling within it. Options are:
  - No fill (**X icon**): removes any fill.
  - Solid blue square: adds a solid color fill to your selection.

![Fill tab options](assets/tools/embroidery/img24.png)

### Stroke paint and stroke style tabs

- Open with Shift + Ctrl + F or via the menu: Object > Fill and Stroke.
- Stroke is the outline or border that goes around the shape. This tab can add or remove a stroke from your selection as well as set its color.
  - No stroke (**X icon**): removes the outline.
  - Solid blue square: adds a solid color outline to your selection.
- The stroke style tab lets you increase the width of the stroke.

![Stroke paint tab](assets/tools/embroidery/img25.png)
![Stroke style tab](assets/tools/embroidery/img26.png)

---

## How to crop an image in Inkscape

1. **Create the shape for cropping:** Create a vector shape (rectangle, circle, star, or custom path) that covers the area you want to keep. Make sure the shape is exactly where you want your crop to be. The shape you use will act like a cookie cutter.
2. **Select both the shape and the image:** Click the shape, hold Shift and then click the image. Both should be selected.
3. **Apply the clip:** Go to Object > Clip > Set Clip. This will hide everything outside the shape, effectively cropping your image.

---

## Ink/Stitch documentation

- Stitch and fill type option documentation: <https://inkstitch.org/docs/stitch-library/>
- Official tutorial YouTube series: <https://inkstitch.org/tutorials/resources/beginner-video-tutorials/>
- Official tutorial articles: <https://inkstitch.org/tutorials/>

## Brother SE700 machine manuals

- Official Brother SE700 support and manuals (Operation Manual, Quick Reference Guide, and more): <https://support.brother.com/g/b/manualtop.aspx?c=us&lang=en&prod=hf_se700eus>

## See Also

- [Sewing Machine](TOOLS/FIBER-ARTS/sewing-machine.md)
- [Tool Training](TOOLS/tool-training.md)
