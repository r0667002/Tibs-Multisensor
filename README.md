# Tibs-Multisensor
This repository includes the necessary code and 3D model for the Tibs Multisensor. The sensor is meant to be **used with Home Assistant** and is created using **ESPHome**. For now, the 3D model is just a prototype and should definitely be improved.

It includes the following components:
- 4x Capacitive touch button TTP223
- 1x PIR sensor AM312
- 1x Rotary encoder KY-040 (rotation + push button)
- 1x Wemos D1 Mini

A possibility would be to add another one like a lux or temperature sensor.

The goal of the project is to make a DIY Light-switch-like control mechanism that can **handle up to 18 different actions** all packaged in a 85x85x11.8mm box. The code for the automations I use is included here as well, to give you some inspiration. I also used a [blueprint](https://community.home-assistant.io/t/trigger-different-actions-on-a-single-double-or-double-click-on-a-binary-sensor/255902) so that different actions can run depending on a single, double or long top on the buttons

## Pinout diagram
The D1 mini itself is powered by a regular 5V adapter plugged into the wall.

![pinout](https://user-images.githubusercontent.com/45207725/153024034-1c3cdfa6-205f-46db-a399-5608fe2a2122.png)

### Important!
Make sure to **connect adjustment pin A on the TTP223 for pin D3**. Otherwise that pin is pulled low and the microcontroller will not boot! The only downside is that the built-in LED on the TTP223 will be on if the button is not pushed. This tends to be visible when using white PLA, so I carefully removed the LED by *sheer brute force*.

For more info about the D1 mini's pinout, look [here](https://randomnerdtutorials.com/esp8266-pinout-reference-gpios/). For more info on the adjustment pins, look [here](https://electropeak.com/learn/interfacing-ttp223-capacitive-switch-butto-touch-sensor-with-arduino/).

## Screenshots
![Front](https://user-images.githubusercontent.com/45207725/152898846-411205eb-df26-4e77-a914-7243cad07b2b.jpg)
![Back](https://user-images.githubusercontent.com/45207725/152899007-e0f0dddb-7d1b-41e9-b92a-ba8064573e5d.jpg)
