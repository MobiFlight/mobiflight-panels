# A320 Autobrake Panel

### Status: Complete - The current PCB (v1.0) has been fabricated and tested.

![Autobrake](https://user-images.githubusercontent.com/2242776/141047958-7eabbc03-5310-4d5b-b7ea-d3f58990a5bb.png)

## PCB Design
The autobrake panel PCB provides it's own functionality and additional external connectivity to the following additional panels, which do not need their own Arduino to operate in this configuration:
 * Brake Pressure Panel: 
   * Three 3-pin headers intended to drive 5V servos for the brake accumulator (BRK_ACCUM) and left and right brake pressure (BRK_PRESS_LEFT and BRK_PRESS_RIGHT)
    * Note: It's recommended that the servos are provided with their own external power source if three servos are being driven. Check the power requirements of your specific servos.
   * Additional LED sinks for backlighting: The 3-pin header (BL_EXT) provides GND sinks to a TCL5917 that can be controlled via the third 8-bit shift register attached to the Arduino (see the schematic for details). 12V for the external LED anodes can be pulled from the 12_HEADER_EXT and grounded back to one of the BL_EXT pins. Typically 2 of these pins are used to drive backlighting in the Brake Pressure (Triple Guage) panel and 1 pin is used to drive backlighting in the landing gear.
 * Landing Gear: A 4-pin header (LDG_GEAR) provides the ability to signal if a separate landing gear lever is in the up or down position, and provides an output to indicate the landing gear warning light (shown within the down arrow).

## Construction of the panel front
The top panel mask is used to group certain Korrys cosmetically. Paint the area inside the masked section around the buttons black after initial cutting. Once the paint has dried, invert the mask and paint the rest of the panel Pigeon Blue (or the color of your choice for panels).

The lower panel, by-design, is larger than the top. This allows the entire panel component to be inserted from back of the MIP or from the top and use the "ears" sticking out to mount to the MIP front panel itself.

 ## 3D Objects Used
 The following files are included for 3D Printing
  - [Korry 389](https://github.com/MobiFlight/mobiflight-panels/blob/main/common/korry/Korry%20Switch%20389%20(3mm%20lens%2C%20B3F-105X%20Switch).stl)
  - [Annunciator-only Korry](https://github.com/MobiFlight/mobiflight-panels/blob/main/common/korry/Korry%20Annunciator%20389%20(3mm).stl)