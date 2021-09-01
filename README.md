# Open Hardware Flight Simulator Panels

MobiFlight uses openly designed Arduino modules to connect buttons and switches and lights to most commonly used flight simulator software. These panels are openly licensed, meaning you can use, improve, share and build them, even for others if you have the skills and tools, but we kindly ask that you share your improvements back to others, if you choose to build upon them. This is a work in progress.

You can configure the panels using Mobiflight, without depending on closed and proprietary drivers and software that might or might not support the simulator software and simulated aircraft of your choice.

## Based on a template system

See the [Mobiflight Panel Template](https://github.com/Mobiflight/mobiflight-templates) for the SVG design asset
library that was used to create these.

These panels are intended for flight simulation, they utilize Arduino hardware, and generally will feature a circuit board
that is mounted behind the panel with 10mm nylon spacers. The finished panels can be connected to Microsoft Flight Simulator 
2020 (msfs2020) or other flight simulator software using Mobiflight open source software. See the 
[MobiFlight website](http://www.mobiflight.com) for more information, and join our Discord server at https://discord.gg/99vHbK7

These are work in progress, contributions are welcome via github pull requests, or if you want to coordinate or have questions, please file an issue.

The design philosophy is to replicate the functionality of real aircraft panels, with realistic looking elements and labeling, but not intending to be a 1:1 accurate replica to the millimeter dimensions. The result look convincing and have the feel of a real airplane cockpits, while enabling you to do 
layouts quickly, and using commonly available hardware as much as possible. 

The panel sizes use the "dzus" mounting standard used in many airplane cockpits, so that different panels can be stacked together and share the same width as much as possible. Some panels naturally might be different like certain panels on A320 center pedestal and overhead panels, but the intention is to adapt the standard as much as practically possible.

## How to edit / view the files

The panel design is a SVG file intended to be used with [Inkscape](http://www.inkscape.org),
and it is laid out with red and black so that it is compatible with a workflow using
[K40 Whisperer](https://www.scorchworks.com/K40whisperer/k40whisperer.html) and a CO2 
laser cutter, to cut and engrave the panels out of acrylic plastic sheet.

The PCB design JSON files can be opened with EasyEDA PCB design suite, accessible at www.easyeda.com. 
On the EasyEDA editor, select "Document" > "Open" > "EasyEDA Source" to import both JSON files into the editor.
One of them is the wiring schema, and the other one is the pcboard itself.

## Mind the gap!

Note, that as this is a pretty monumental work in progress, and the idea is to do this together as a community, we try to share designs earlier rather than later. For this reason, designs might not be final, complete or even fully functional, although we try to have functional stuff in the repository. When some
designs depend on certain 3D-printed button gaps or other hardware, that should be ideally noted in the README file.



