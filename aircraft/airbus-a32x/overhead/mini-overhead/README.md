# A320 Mini Overhead

A small panel that encompasses many of the A320 overhead features into a small package to enable flight with minimal keyboard and mouse input for the overhead.

### Status: **Complete** - The current PCB (v1.0) has been fabricated and tested.

![Mini Overhead](https://user-images.githubusercontent.com/2242776/149878500-271aab1d-ab63-4d59-a4bd-bb05953e75b0.jpeg)

The panel is comprised of three layers, starting with the frontmost (user-facing) layer and moving backward as defined in the [A320 Mini Overhead SVG File for Laser Cutting](https://github.com/ssewell/mobiflight-panels/blob/main/aircraft/airbus-a32x/overhead/mini-overhead/a320-mini-overhead.svg)

- 3mm white acrylic, laser cut, painted Pigeon Blue, then laser etched
- 3mm clear acrylic, painted black in non-masked areas
- PCB

## 3D Objects Used

The following files are included for 3D Printing

- [Korry 389](<https://github.com/MobiFlight/mobiflight-panels/blob/main/common/korry/Korry%20Switch%20389%20(3mm%20lens%2C%20B3F-105X%20Switch).stl>)
- [ADIRS Knob](https://github.com/MobiFlight/mobiflight-panels/blob/main/common/knob/EFIS-Knob.stl) (ADIRS knob uses the same model as the EFIS design)

## Electronic Component Listing

The electronic component listing for the circuit can be found within the EasyEDA schematic standard BOM listing.

## MobiFlight Configuration

In the included MobiFlight config files, many of the sim functions are combined into a single button/switch (i.e. pressing the fuel pump button will toggle all fuel pumps at the same time).

The switches to control the lighting have the following attributes:

- EXT LT (3 pos):
  - Up: Strobe: On, Beacon: On, Nav & Logo: On
  - Mid: Strobe: Auto, Beacon: On, Nav & Logo On
  - Down: All off
- Nose (3 pos):
  - Up: RWY TURN OFF: On, Nose: T.O.
  - Mid: RWY TURN OFF: On. Nose: TAXI
  - Down: RWY TURN OFF: Off, Nose: Off
- Land (3 pos):
  - Both landing lights: On
  - Both landing lights: Off
  - Both landing lights: Retracted
