# Polar Plotter

![alt text](./images/image.png)

Experimental plotter. It runs under Kalico and uses klipper polar kinematics.

Polar plotter is driven by [VØ](https://github.com/fbeauKmi/v-nothing)

## Bill of Materials

| **Hardware**            | **Quantity** | **Notes**                          |
|--------------------------|--------------|-------------------------------------|
| Stepper Nema17           | 2            |                                     |
| Servo Savox SH0255 or M90s | 1          |                                     |
| Linear Rail MGN9C 150mm  | 1            |                                     |
| Open Belt GT2 6mm 514mm  | 1            |                                     |
| Loop Belt GT2 6mm 300mm  | 1            |                                     |
| GT2 Gear 20T 6mm         | 2            |                                     |
| Bearing F623zz           | 8            |                                     |
| Bearing F695zz           | 2            |                                     |
| Rod D3mm 75mm            | 2            | Sourced from an old DVD writer      |
| BHCS, SHCS M3/M5 Screws & Nuts | -            | Minimal quantity required           |
| SBC and MCU              | 1            | Use a [VØ](https://github.com/fbeauKmi/v-nothing) |
| Permanent marker | 1 | [Sharpie Ultrathin](https://www.amazon.com/Sharpie-37001-Permanent-Markers-Ultra/dp/B00006IFI7) or [Staedler Lumocolor 313](https://www.amazon.de/-/en/Staedtler-313-WP4-Universal-Lumocolor/dp/B0007OEDQQ) | 


## G0 macro override
To avoid crossing 0,0
G1 moves (drawing) are "linear" and G0 moves (travel) are polar

see [printer.cfg](./config/kalico/config/printer.cfg) for configuration

## Write G-Code from SVG
### Draw your model with Inkscape
Kinematic size is 120mm in diameter
Use model [DVD_label.svg](./config/svg/DVD_label.svg) as example

Extensions like Eggbot Hatch fill or Hershey Text can be useful for a plotter use


### KPolar
I use [KPolar](https://github.com/fbeauKmi/KPolar) a fork of [GRBL-Plotter](https://github.com/svenhb/GRBL-Plotter)
to convert SVG into gcode and send it to the plotter via Moonraker API.

