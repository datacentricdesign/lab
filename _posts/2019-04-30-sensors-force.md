---
layout: post
comments: true
title:  "Force Sensing Resistors"
date:   2019-04-30 01:30:13
image: '/assets/img/'
description: Some info about force sensors
main-class: 'tutorial'
color:
tags: sensor, force, FSR
categories:
twitter_text:
introduction:
---



# Force Sensing Resistors (FSRs)
FSRs are a type of robust polymer thick film (PTF) that decrease in resistance with an increase of force applied to the surface of the sensor. We will be Working with the interlink FSR 406.
The interlink is part of the single zone FSRs family, with optimized force sensitivity for use in human touch control of electronic devices.

![Force Sensing Resistors](/lab/assets/img/posts/force_2.png)

## Technical Details

* Sensitivity range from 0.1N to 100N of force;
* 0.45mm thick;
* Handles up to 10M actuations;
* 10MΩ when non actuated;
* Non linear Resistor, so changes of force are not linear to changes in resistance, especially in the end of the sensing range (~4V and up);


## Examples

### Pressure Sensor with Sampling and Basic Filtering
Lets make a pressure sensor using a voltage divider circuit and the arduino!

#### Schematic
The common way to use this transducer is with the use of a voltage divider circuit. $R_1$'s value will change the way the voltage curve(for $V_1$ ) is for different pressures (the lower the resistance,  the more low pressure values are spread out, and the curve becomes more 'stretched'), lets see a common voltage divider, and our particular case:

![Schematic](/lab/assets/img/posts/force_3.png)

Here's the whole sensor system diagram:

![Sensor system diagram](/lab/assets/img/posts/force_4.png)

You can find the example of code [here](https://github.com/datacentricdesign/lab/blob/master/examples/sensors/force/fsr_406/fsr_406.ino).


#### Results
Let's see what the console looks like in the end!

![Result](/lab/assets/img/posts/force_1.gif)


You can find an example of code with 12 FSR 
[here](https://github.com/datacentricdesign/lab/blob/master/examples/sensors/force/fsr_406_x12/fsr_406_x12.ino).
