# A320 MCDU panel

This panel is designed around the Arduino mega pro mini for 
use with Mobiflight. Due to limited pins on the core arduino, 
the OVFY, AIRPORT, SEC F.PLN, BRT and DIM buttons are 
connected to a secondary arduino pro micro mounted alongside.
The LED indicators are also connected to this secondary arduino
to be fully functional.

## Features:

**LED Backlighting** - 12V supply powers the led backlight, 
pin13 on the arduino controls the brightness of them via 
a FET, if you prefer to control the brightness by varying 
the voltage instead, this is possible by bridging pins 2 
and 3 of the FET pads on the PCB.

**LED indicators** - all LEDs and resistors are able to be 
either traditional components ie. 3mm LED or surface 
mount components.

**Additional function buttons** - If discreet additional 
function buttons are desired they can be put in place of
the top 5 indicator LEDs and used for functons such as 
TO Config, Cabin Call or any other function that is desired.

This is DZUS mount compliant so it will fit in any cockpit 
using this mounting system (although this is optional).

All required Mobiflight configuration files are attached.

The.svg file to print/cut your own front panel and keys is 
also attached.

Windows Layout Manager and the pre-written configuratioon 
have been attached as a .zip to spread the screen to the 
edge properly on the MCDU.

This design also matches the Opencockpits panel footprint.

**Button caps for resin pritners** - Special design for resin printers. Print with white resin, spray with black acrylic paint and engrave letters, numbers and symbols with CO2 laser. Only 3 designs available now (numbers, letters, line select), we are working on the rest. Usable with 3+3+3mm MCDU panel. Fusion 360 source files will be available after all buttons will be ready.

![image](https://user-images.githubusercontent.com/13331823/157750405-e8288548-f697-4958-ab13-5291bc08442f.png)
