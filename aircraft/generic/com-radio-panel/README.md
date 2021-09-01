# Generic Airliner-style radio panel

This design can have one to three buttons on the front panel, like this example has COM1 and COM2 selectors, 
and a BOTH button so that it can work a bit as an audio panel too, in case you don't have a separate audio
panel. Or you can leave them out if you want to build separate COM1, COM2, NAV1, NAV2 radios, just don't solder 
the buttons and leds, and remove the cutouts from the panels.

![image](https://user-images.githubusercontent.com/2587818/131249004-59448b31-ed80-4a01-8a27-8274ee582d79.png)

The included configuration file makes it work as a combined COM1+2 radio for MSFS2020, but naturally this
can be changed with MobiFlight if you wish.

## Parts

The encoder used is the ALPS EC11EBB24C03 that I found from Aliexpress. The pushbuttons are 
[Multimec 3FTH9](https://octopart.com/3fth9-mec+switches-49180836).

The pcb has 2 through-hole MAX7219 chips, 1206 size SMD leds, BS170 FETs to dim the leds from one pin, 
some 1206 surface mount resistors and two capacitors for each MAX chip as recommended by its datasheet. 
The yellow 7-segment displays are common cathode 0.28 inch tall units of 3 digits each.
