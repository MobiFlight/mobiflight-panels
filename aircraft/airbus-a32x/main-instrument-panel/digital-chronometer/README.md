# A320 Digital Chronometer

![Digital Chronometer](https://github.com/MobiFlight/mobiflight-panels/assets/2242776/7040894c-ee18-493b-9b2d-d188d002a161)

## Overview

To build this guage, in addition to a CNC laser capable of cutting acrylic, you'll need:

- 7 mm standoffs (must be cut to size of approximately 6.5mm, adjust as needed)
- Various M3 nuts and bolts
- Various electronics as indicated in the BOM (The BOM can be viewed in EasyEDA after opening `SCH_A320 Chrono.json`)

## Laser Cutting

Laser cutting instructions for the layers indicated in the SVG file.

Two design have been included in the SVG. Choose which option works the best for your available materials and preferences:

### Clear Bottom Layer with masked windows (Option 1)

- All laser operations are performed from the back (SVG should mirrored)
- Mask clear acylic using layers `Bottom Panel Tape Mask (back paint style)` (blue lines) and paint black from the back side
- Once paint has dried, ablate paint using the `Bottom Panel Blue Text` and `Bottom Panel` layers (black text) and cut (red lines)

### White Bottom Layer with cut windows (Option 2)

- All laser operations are performed from the front (SVG NOT mirrored)
- Mask white acrylic using layer `Bottom Panel Tape Mask (front paint style)` and paint black
- Once paint has dried, ablate paint using the `Bottom Panel` layer (black text) and cut (red lines)

### Top Layer (common to both options above)

- Paint white acrylic pigeon blue, ablate paint using `Top Panel` layer (black text) and cut (red lines)
