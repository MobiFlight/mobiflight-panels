# A320 Brake Pressure Gauge

![Brake Pressure Gauge](https://user-images.githubusercontent.com/2242776/145629269-c75f62d5-ccfd-46e7-94d3-89705cca52d4.png)

Flush mount example shown above, without color transparency layer

This panel design doesn't include a PCB design as the servos are driven by the [Autobrake Panel](https://github.com/MobiFlight/mobiflight-panels/tree/main/aircraft/airbus-a32x/main-instrument-panel/autobrake).
Currently, these are more rough notes than a comprehensive how-to.

## Overview
To build this guage, in addition to a CNC laser capable of cutting acrylic, you'll need:
 * Various standoffs, M3 screws and nuts
 * Three SG90 servos
 * Small wooden or metal rods that will drive the needles. The rod should be approximately 2mm in diameter. Exact measurement that will fit into the SG90 servo needs to be determined, as I used toothpicks. If you use a metal rod and find a good fitting, please let us know on our Discord server [MobiFlight](https://discord.gg/y4mChQ59) so we can update this doc.

 All acrylic used is 3mm thick.

## Laser Cutting
 Laser cutting instructions for the layers (starting from the bottom and working up) indicated in the SVG file
 * **Servo Mounting Plate**: Simply cut as indicated by red lines. Acrylic color isn't important
 * **Display Plate**: White acrylic, cut as indicated by red lines. Paint black, then raster etch black areas
 * **Display Plate Transparency Print**: Optional, color printed on transparency to be added on top of the display plate to add the green sections to the guages
 * **Middle Layer Spacers**: Cut indicated by red lines. Pained the color of your choice. Make two of these.
 * **Top Cover**: Use clear acrylic. Mask out the blue area by leaving the protective paper (or adding your own masking tape), and use the laser on an extremely low setting to score the protective paper. Cut inidicated by red lines. Remove the mask covering from the outer area (leaving the circle intact), and paint the color of your choice. Remove the mask, leaving the center circle clear.
* **Needle**: Use white acrylic. Position these as needed on your own stock. You'll need three needles. Create mask using the same procedure as the top cover to paint the large circle section of the needle black. Once the paint is dry, place the needles paint side down, and etch an indentation (about 3/4 of the way through) to provide mount points for the servo rods.

## Backlighting
For backlighting I used a small perfboard with LEDs mounted via standoffs by the way of the two innermost holes
![Gauge face mounts](https://user-images.githubusercontent.com/2242776/145620612-afa41d7f-9a0d-44af-b3f1-026570a0f682.png)

## Assembly
Assembly including backlighting can be a bit tricky. I used this procedure:
 * Mount the servos to the servo mounting plate using M3 screws and nuts
 * Insert the servo rods into servos
 * Affix the standoffs to the servo mounting plate, with the female end facing upwards
 * Affix the standoffs to the LED perfboard, with the female end facing upwards (same direction as the LEDs)
 * Partially assemble the guage (bottom panel, perfboard, display plate), holding the perfboard standoffs firmly against the back of the front plate
 * Add short standoffs (length depends on your particular mounting needs) to the four inner holes (this attaches the back panel servo bracket to the front panel, and provides additional mount points accessble from the front)
 * Push the needles onto the exposed servo rods on the display plate
 * Add the top cover layers and use the two remaining holes to affix the faceplate, which holds the backlight board in place from below
