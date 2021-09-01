Citation CJ4 electrical power

This panel contains the main power switch and other related controls for the 
Working Title Cessna Citation CJ4.

![image](https://user-images.githubusercontent.com/2587818/131339999-8c6e6d0a-e69b-46cb-b83d-db3340d008c3.png)

Some things are not fully implemented in the simulator, like Generator resets,
and Emergency lights "Armed" vs "ON" mode. Also, the standalone artificial 
horizon "test" mode is just done by using the momentary switch to turn it on,
so it turns off when the switch is released.

Included are the Mobiflight Arduino configuration file, and a Mobiflgiht Connector configuration file to use 
this panel with the WT CJ4, as well as SCH and PCB files for EasyEda circuit board design tool.

![image](https://user-images.githubusercontent.com/2587818/131340632-c589d045-22eb-49ba-a85d-4bf7b6fd52b6.png)

## Parts 

The PCB uses an Arduino Pro Micro, and 12V input for the backlight, dimming is done with a BS170 N-channel FET, which
has a rather tiny footprint on the PCB, making it slightly trickier than usual to solder. I only realized this after
ordering my pcb's. Something to be aware of - though I don't consider myself a super soldering expert, and I managed to solder 
the legs without connecting them together with a blob of solder, so I guess it'll be fine if you just work carefully and have
thin solder and iron tip.

Switches are the "SH T80-T Z1 Series" toggle switches from Aliexpress, which have a large metal handle but a micro-sized switch body
and solderable feet for pcb. The main power switch has a piece of red heatshrink on the lever. Three switches are ON-OFF-ON type,
and three (generators and the standby artificial horizon) are ON-OFF-MOM, meaning a three position switch where one side
returns to center with a spring.
