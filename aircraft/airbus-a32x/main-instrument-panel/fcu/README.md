# A320 FCU (Flight Control Unit)

### Status: **Untested** - The PCB (v1.0.2) is functionally complete, but untested. Version 1.0 was used to produce the following FCU, but it requires a bodge that is corrected in v1.0.2.

![FCU Picture](https://user-images.githubusercontent.com/2242776/132795702-47a3354e-0c7d-40a7-af49-7301dd092763.jpg)

The current design forgoes the 100/1000 rotary switch selector nested in the ALT push-pull encoder to simplify the internal implementation. Instead, a 100/1000 pushbutton has been placed below the METRIC ALT button.

The panel is comprised of three layers, starting with the frontmost (user-facing) layer and moving backward
 - 3mm white acrylic, laser cut, painted Pigeon Blue, then laser etched
 - 3mm clear acrylic, painted black in non-masked areas, then laser etched
 - PCB

## Electronic Component Listing
[Electronic Component Listing forthcoming]

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

 This example of the PCB (as viewed from the *back*), shows the pin indicating to the push-pull encoder mechanism's PUSH feature for the SPEED knob in the top-right position:
 ![PCB Header Closeup](https://user-images.githubusercontent.com/2242776/132797899-5f7ce723-6485-41d5-84f1-227561c238dd.jpg)

 Keep in mind the speed knob is the leftmost knob when viewing the PCB from the *front*.

## Attachment of the Push-Pull Encoder Mechanism
Each push-pull encoder mechanism is attached to the back of the clear acrylic layer using two countersunk M3 screws with a corresponding bolt to hold them in place from the back. Due to the proximity of the countersunk holes to the larger hole rotary encoder hole, great care should be taken to not apply excessive pressure when creating them with a countersink tool.