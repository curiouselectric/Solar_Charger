# DIY Solar Charger Kit

# Overview

This is a DIY solar LiIon charger unit. It is designed to run small electronics projects (such as data-loggers and environmental monitoring units) in places where there is no supply of electricity. I designed it originally to run a small weather station which monitored and wirelessly sent back data to a base station.

It uses the [Texas Instruments BQ24210](http://www.ti.com/product/BQ24210).

This is a 800mA single-input, single cell Lithium Ion battery charger IC.
The datasheet is available here: http://www.ti.com/lit/ds/slusa76b/slusa76b.pdf

This IC is great and required very few external components, but it is quite an expensive IC and also it is only available in a WSON-10 pin surface mount package. This is impossible to solder by hand. For this kit we pre-solder this component for you. All the other parts are through-hole and can be soldered by hand.

The kit uses 2 x 1W 5V solar PV cells (connected in parallel).

This IC is used to recharge a single 18650 LiIon cell, which are widely available in a range of capacities.

The output can be used directly, as the voltage of the LiIon cell (around 3.7-4.4V DC). This can be used on micro-controller projects, such as data-loggers and weather stations which might need a local source of reliable, off-grid power.

There is also a DC/DC converter unit to provide a 5V output. The 5V output is switched. 
The 5V output can be used to power USB devices or your microcontroller projects.

## PCB overview

This repository contains the [KiCad](http://kicad-pcb.org/) PCB design files.

The PCB is quite simple.

*** photo of circuit board and features ****


## Hardware overview

The hardware design files are available in this repository.
These parts are laser cut and are supplied with the kit. You will need to use some silicone sealant if you would like to make this unit waterproof.

Other options for this kit are to use a water-tight box (such as a lunchbox) and have to solar panels on the outside of this. This would be a low-cost and easy to obtain enclosure.


## Energy available

The energy output depends upon the sunlight available.
In the UK the 2W of solar panels will provide around 8Wh per day in summer and 2Wh per day in winter.

### Usage example

You would like to power an Arudino data-logger which uses 20mA at 5V. Would this work in the UK throughout the year?

So the logger will consume:

Power: 20mA = 0.02A times 5V = 0.1W - This is the power consumed constantly.
Energy: 0.1W x 24 hours = 2.4Wh per day.

So this unit will work OK through spring/summer/autumn, but it might not be OK through the winter.

Energy could be saved by redcuing the load (such as removing voltage regulators that are not required) or by clever use of sleep modes.

We have used an Arduino Nano with minimal changes (removed power LEDs and voltage regulator) and this has given us an average power consumption of around 1.5mA, which is just 0.0075W = 7.5mW.

## To Do

* Hardware design
* Instructions
* Photos of build
* Installation examples
* Put for sale
