# Changelog

## 2021-09-08

* Added the new "Made for ESPHome" logo to the design and README.md.
* Updated the project to change its name to "DSMR Reader for ESPHome".
* Added the 3D printing STL files to the project.

## 2021-09-03

* Swapped out the RJ12 connector part with another one, that has the soldering holes a bit closer to each other. With the original part, I had to bend the connector pins a bit to get them to fit in the holes.
* Added a 100nF capacitor to the reset switch connector for debouncing button presses.
* Rearranged the board to remove all components from under the ESP-01 MCU. This makes it easy to solder the ESP-01 directly onto the board if one desires to do so.
* Made the mounting holes a bit bigger to allow the use of M3 screws.

## 2021-08-28

* Changed the placement of the ESP-01, to bring the WiFi antenna to the outside of the board. Thanks to Frank Bakker on the ESPHome Discord for asking me why I hadn't done so. I had no answer to that :-)
* Exposed all pins that are required for flashing to the breakout header (practically meaning: I added the RXD header), as requested by Frnk.
* To make flashing easier, I added two jumpers that can be used for resetting and putting the ESP-01 into flash mode (i.e. connecting GPIO0 to GND).
* Improved the routing of a 3.3V trace. Thanks to Azimath on the ESPHome Discord.
* Fixed the use of the wrong voltage regulator (change LM1117 to AMS1117). Thanks to Azimath for the heads up.

## 2021-08-27

* Use thermal isolation for the ground pads to make soldering easier. Thanks to Azimath on the ESPHome Discord.

## 2021-08-26

* Added a breakout header for exposing 3V3, GND and unused pins (GPIO0, GPIO2, TXD). Thanks to Frank Bakker on the ESPHome Discord.
* Various small layout changes. Thanks to Jos (and his OCD) on the ESPHome Discord.

## 2021-08-24

* Introduced a jumper that can be used to enable or disable the 1000 uF capacitor for DSMR v4 compatibility. When using the board directly for a DSMR v5 meter, then the capacitor can be omitted. The main idea of the jumper is to make it possible to move from a DSMR v4 to a DSMR v5 meter by simply removing the jumper.
* The GND at the bottom side is now implemented using a copper pour. Thanks to stoic on the ESPHome Discord.

## 2021-08-23

* One less 1000 uF capacitor, a single one is all we need here (I'm running on a v4.2 here with 1000 uF installed, and it's running very stable).
* Added the jumper for enabling the 1000 uF for DSMR v4.
* RST is now pulled high using a 10k resistor (I had no problems with it being floating in the previous design, but better make that an explicit pull up).
* Added a 100 nF capacitor on the input side, because that was suggested in the DSMR v5 companion documentation.
* Moved the RJ12 connector a bit outside the board, to make it easier to expose it from an enclosure.
* Added some holes at the corner so it can be screwed into an enclosure.
* Did some manual routing, to have all routes on top of the board, except for GND which is routed via the bottom of the board.
* No traces below the antenna of the ESP-01. I use a 2x4 header there, making the ESP-01 float 12mm above the board, so I have no problems with the antenna. But keeping the area free of traces should allow one to solder the ESP-01 directly onto the board. Thanks to stoic on the ESPHome Discord.
* Added debug pads for easier trouble shooting.

## 2021-07-23

* Initial circuit and board layout created.
