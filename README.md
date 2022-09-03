## Sept22 - This repository NOT ready for consumption yet...

## Let me explain what I'm doing with this repository...

I will not post full source code here.  Source code is a work product that I like to get paid for doing.   What I will post are flow charts, state transition diagrams, block diagrams, and explainations on what makes the project work.  There will be some source here, but only enough to substantiate my expertese in the subject.

#### Please view the README.md files in subdirectories for helpful info.

### What this project covers:
I have integrated the AWS ESP demos into one project.  Typically, I just reverse engineer their algorythms and then unifiy them.  This covers the following features:
* MQTT Client
* Fleet Provisioning
* Thing Shadow
* OTA Update

### AWS IOT Device SDK for Embedded C
The Espressif people are not super good at getting solid workable code in their SDK.   I have managed to get their March 2021 release to work for me.  There may be very tiny adjustments in this library so I have posted my copy of the library here.  NOTE: the "port" directory in the root of the project is part of that library.  So take care to get both:
* aws-iot-device-skd-embedded-C
* port

I will update all the documentation and the library which supports it in the future.  If you have confidence in my work, and you have a budget to pay for my assitance, I'm happy to work out an exchange with you.  This library is complicated and you will need some help if you lack the mental focus on what is required.  This is not a casual effort.
