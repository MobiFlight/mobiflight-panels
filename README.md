# Flight Simulator Panels

See the [Mobiflight Panel Template](https://github.com/Mobiflight/mobiflight-templates) for the SVG design asset
library that was used to create these.

These panels are intended for flight simulation, they utilize Arduino hardware, and generally will feature a circuit board
that is mounted behind the panel with 10mm nylon spacers. The finished panels can be connected to Microsoft Flight Simulator 
2020 (msfs2020) or other flight simulator software using Mobiflight open source software. See the 
[MobiFlight website](http://www.mobiflight.com) for more information, and join our Discord server at https://discord.gg/99vHbK7

These are work in progress, contributions are welcome via github pull requests, or if you want to coordinate or have questions, please file an issue.

## How to edit / view the files

The panel design is a SVG file intended to be used with [Inkscape](http://www.inkscape.org),
and it is laid out with red and black so that it is compatible with a workflow using
[K40 Whisperer](https://www.scorchworks.com/K40whisperer/k40whisperer.html) and a CO2 
laser cutter, to cut and engrave the panels out of acrylic plastic sheet.

The PCB design JSON files can be opened with EasyEDA PCB design suite, accessible at www.easyeda.com. 
On the EasyEDA editor, select "Document" > "Open" > "EasyEDA Source" to import both JSON files into the editor.
One of them is the wiring schema, and the other one is the pcboard itself.



