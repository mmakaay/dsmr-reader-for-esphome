# Changelog

## 2021-08-26

* Added a breakout header for exposing 3V3, GND and unused pins (GPIO0, GPIO2, TXD). Thanks to Frank Bakker on the ESPHome Discord for the suggestion.
* Various small layout changes. Thanks to Jos (and his OCD) on the ESPHome Discord for the suggestions.

## 2021-08-24

* Introduced a jumper that can be used to enable or disable the 1000 uF capacitor for DSMR v4 compatibility. When using the board directly for a DSMR v5 meter, then the capacitor can be omitted. The main idea of the jumper is to make it possible to move from a DSMR v4 to a DSMR v5 meter by simply removing the jumper.
* The GND at the bottom side is now implemented using a copper pour. Thanks to stoic on the ESPHome Discord for the suggestion.

## 2021-08-23

* One less 1000 uF capacitor, a single one is all we need here (I'm running on a v4.2 here with 1000 uF installed, and it's running very stable).
* Added the jumper for enabling the 1000 uF for DSMR v4.
* RST is now pulled high using a 10k resistor (I had no problems with it being floating in the previous design, but better make that an explicit pull up).
* Added a 100 nF capacitor on the input side, because that was suggested in the DSMR v5 companion documentation.
* Moved the RJ12 connector a bit outside the board, to make it easier to expose it from an enclosure.
* Added some holes at the corner so it can be screwed into an enclosure.
* Did some manual routing, to have all routes on top of the board, except for GND which is routed via the bottom of the board.
* No traces below the antenna of the ESP-01. I use a 2x4 header there, making the ESP-01 float 12mm above the board, so I have no problems with the antenna. But keeping the area free of traces should allow one to solder the ESP-01 directly onto the board. Thanks to stoic on the ESPHome Discord for the suggestion.
* Added debug pads for easier trouble shooting.

## 2021-07-23

* Initial circuit and board layout created.
