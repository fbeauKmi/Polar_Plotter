# Polar Plotter

![alt text](./images/image.png)

Experimental plotter. It runs under Kalico and uses klipper polar kinematics.

Polar plotter is driven by [VØ](https://github.com/fbeauKmi/v-nothing)

# G0 macro override
To avoid crossing 0,0
G1 moves (drawing) are "linear" and G0 moves (travel) are polar

see [printer.cfg](./config/kalico/config/printer.cfg) for configuration

# Write G-Code from SVG
## Draw your model with Inkscape
Kinematic size is 120mm in diameter
Use model [DVD_label.svg](./config/svg/DVD_label.svg) as example

Extensions like Eggbot Hatch fill or Hershey Text can be useful for a plotter use


## KPolar
I use [KPolar](https://github.com/fbeauKmi/KPolar) a fork of [GRBL-Plotter](https://github.com/svenhb/GRBL-Plotter)
to convert SVG into gcode and send it to the plotter via Moonraker API.

