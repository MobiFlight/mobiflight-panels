# A320 FCU (Flight Control Unit)

### Status: **Untested** - The current PCB (v1.0.3) is functionally complete, but untested. Version 1.0 was used to produce the following FCU, but it required a bodge that was corrected in v1.0.2.

![FCU Front](https://user-images.githubusercontent.com/2242776/133118930-89cbbde2-fbe4-4aab-bdd7-f9aa332fe413.jpg)

The current design forgoes the 100/1000 rotary switch selector nested in the ALT push-pull encoder to simplify the internal implementation. Instead, a 100/1000 pushbutton has been placed below the METRIC ALT button.

The panel is comprised of three layers, starting with the frontmost (user-facing) layer and moving backward as defined in the [A320 FCU SVG File for Laser Cutting](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/airbus-a32x-fcu.svg)
 - 3mm white acrylic, laser cut, painted Pigeon Blue, then laser etched
 - 3mm clear acrylic, painted black in non-masked areas, then laser etched
 - PCB

 ## 3D Objects Used
 The following files are included for 3D Printing
  - [Korry 389](https://github.com/MobiFlight/mobiflight-panels/blob/common/korry/Korry%20Switch%20389%20(3mm%20lens%2C%20B3F-105X%20Switch).stl)
  - [Korry 307-like](https://github.com/MobiFlight/mobiflight-panels/blob/common/korry/airbus-a32x/glareshield/fcu/Korry%20Switch%20307-like%20(3mm%20lens%2C%20B3F-105X%20Switch).stl)
  - [Push-Pull Frame](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/Push-Pull%20Frame%20(B3F-105X%20Series).stl)
  - [Push-Pull Slider](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/Push-Pull%20Slider%20(B3F-105X%20Series).stl)
  - [ALT Knob](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/FCU%20Knob%20(ALT%2C%2014mm%20Skirt%2C%206.7mm%20Hole).stl)
  - [HDG Knob](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/FCU%20Knob%20(HDG%2C%2014mm%20Skirt%2C%206.7mm%20Hole).stl)
  - [SPD Knob](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/FCU%20Knob%20(SPD%20%26%20VS%2C%2014mm%20Skirt%2C%206.7mm%20Hole).stl)
  - [V/S Knob](https://github.com/MobiFlight/mobiflight-panels/blob/main/aircraft/airbus-a32x/glareshield/fcu/FCU%20Knob%20(SPD%20%26%20VS%2C%2014mm%20Skirt%2C%206.7mm%20Hole).stl) (Currently same as the SPD)

## Electronic Component Listing
The electronic component listing for the circuit can be found within the EasyEDA schematic standard BOM listing.

The additional components are required for the Push-Pull Encoder mechanism (described below)

| Component | Manufacturer | Part Number | Quantity | Comments
| - |- | - | - | -
| Tactile Button | 	Omron Electronics | B3F-105X | 8 | The X in the part number can be replaced with the appropriate number to signifiy the force required to press the button of your own preference
| Rotary Encoder | Bourns | PEC11R-4220F-N0024 | 4 | You do *not* want an encoder with an integral switch (button) feature, as the Push-Pull Encoder Mechanism handles this
| Perfboard |||| Must be cut into sizes that fit the 3D printed push-pull encoders (shown below)

## Push-Pull Encoder Mechanism
The three rotary encoders provide a push-pull feature, similar to the real Airbus A320. This implementation uses tactile buttons that provide a click feedback when using the feature.

The four push-pull encoders must be 3D printed, each one having two main parts: A slider in which the rotary encoder is mounted, and the frame that holds the two buttons for the push-pull feature. The STLs are in this folder, starting with the name "Push-Pull Slider"

![Push-Pull Encoder Mount](https://user-images.githubusercontent.com/2242776/132796173-a47dbb3f-043a-455c-9826-34de717b2fec.jpg)

Here's a print, showing the placement of the perfboard prior to soldering the tactile buttons.
![3D Print of Push-Pull Slider](https://user-images.githubusercontent.com/2242776/132796985-3013e505-e886-4e21-b403-84c06be06381.png)

Once full assembled, you should have 5 wires attached to the device for each of the functions:
 - Rotate Left
 - Rotate Right
 - Push
 - Pull
 - Ground (common to the encoder and buttons)

You should connect each of these to a header that will match the back of the PCB, where these will be ultimately connected once the panel is assembled.

The PCB has 4 sets of 5x1 header with a standard 2.540mm pitch. You can mount either the male or female header to the PCB, just ensure you use the opposing gender connector for the push-pull encoder wiring.

Each of these four sets have the following lettering for the first character of the corresponding control silkscreen marking:
 - S = Speed
 - H = Heading
 - A = Altitude
 - V = V/S

 These same four sets have the following lettering for the second character of the corresponding control silkscreen marking:
 - L = Left (encoder)
 - R = Right (encoder)
 - P = Push (button)
 - U = Pull (button)

 The bottom pin on all of these sets are GND.

 This example of the PCB (as viewed from the *back*), shows the pin indicating to the push-pull encoder mechanism's PULL feature for the SPEED knob in the top-right position:
 
 ![PCB Header Closeup](https://user-images.githubusercontent.com/2242776/132797899-5f7ce723-6485-41d5-84f1-227561c238dd.jpg)

 Keep in mind the speed knob is the leftmost knob when viewing the PCB from the *front*.

## Attachment of the Push-Pull Encoder Mechanism
Each push-pull encoder mechanism is attached to the back of the clear acrylic layer using two countersunk M3 screws with a corresponding bolt to hold them in place from the back. Due to the proximity of the countersunk holes to the larger hole rotary encoder hole, great care should be taken to not apply excessive pressure when creating them with a countersink tool.

## 7-Segment Display Windows
The "windows" that appear at the top of the FCU are acrylic of the same depth as the frontmost (user-facing) panel cut to the same size as the openings. Using a "K40 Laser" yielded a window that could easily be press-fit into the openings without any adhesive due to the inherent imperfections in the cut edge.

You can use colored acrylic to provide a nice tint to the LEDs in the event you used white 7-segment modules. If you chose to use colored 7-segment modules, the light emitted is often a narrow band, so colored acrylic has little to no effect.

Before cutting the acrylic windows, you can apply a tinted adhesive sheet that will increase the contrast of the LEDs. The cutting action will also weld the outer edge of the tint to the acrylic itself, which prevents peeling. Try to avoid a tint film that has "air-release" designed for air bubble prevention, as its texture is often visible when the LEDs are lit from behind. It's recommended that you mount the windows, tint facing inwards, to minimize blur, which gives the window surface a nice clean appearance.
