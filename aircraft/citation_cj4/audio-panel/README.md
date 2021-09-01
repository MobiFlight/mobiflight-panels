# Cessna Citation CJ4 audio panel

This is using potentiometers, lots of potentiometers. In fact, more than what MobiFlight can currently handle.
Also, a lot of the switches are not functional in MSFS2020. So it is mostly for the looks, but the COM1+2 adjustment
is really nice in practice, especially when flying in VATSIM/IVAO/PilotEdge.

![image](https://user-images.githubusercontent.com/2587818/131625742-8e15e307-1464-4f22-8521-6c8a26fdc299.png)

But the upside is, you can also configure a potentiometer as a toggle switch, and it will flip over at the 
midpoint of the potentiometer, so you get the same look and feel of a volume knob, but with the functionality of a 
switch, which works pretty nicely here, as most of the audio panel potentiometers in MSFS2020 work as a switch 
only anyway.

![image](https://user-images.githubusercontent.com/2587818/131628341-7e8149b0-6649-49e1-ad77-07f615080041.png)

## Parts

<img src="https://user-images.githubusercontent.com/2587818/131629134-9228db7b-97bf-4b9e-bdee-544b4e7d3a41.png" align="right" alt="led insertion to panel" />

The indicators are 3mm leds, you should use black nail polish to mask the sides of the leds dark, so that they will not get diffused light from the panel backlight, as they will be embedded in the white acrylic.


The "SR16 3 position rotary switch" from aliexpress had a mismatch with the pinout, it seems to connect pins 2-3-4 on positions 1-2-3, this is corrected on the pcb but my own variant does not do this. The switch itself is pretty much non-functional on the sim anyway, so it does not really matter much in practice, b
## Configuration

Configuration is not finished yet, there is a .mcc file that defines volume knobs for COM1 and COM2, and the transmit led + buttons, but not much else yet. Also included is a pin configuration file for flashing the arduino. It uses an arduino Mega Pro Mini and has 12V input for backlighting leds.
