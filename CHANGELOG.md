# Changelog

## 2021-11-06

* Initial release of my DSMR reader for ESPHome, based on the ESP8266 D1 Mini.
* The design uses the "Made for ESPHome" logo, approved by Nabu Casa.
  See: https://esphome.io/guides/made_for_esphome.html
* A few PCB versions and styles were explored, before ending up with this version: D1-DS-3.
  This code indicates the third iteration of a D1 mini-based Display Shield solution.
* Earlier versions did use some SMD components, but those can be a bit of a challenge for people
  with limited soldering tools / skills. Therefore, this version uses only through hole components,
  that are not hard to solder.
* The circuitry provides hardware support for inverting the UART signal, as required for a P1 port.
* It also provides support for enabling and disabling the P1 request data pin. Using this, the
  update interval for the smart meter readings can be cleanly controlled. Also, the data transmissions
  from the smart meter can be suspended after reading a telegram, so no new data will come in during
  processing of the telegram. This is especially useful for those meters that are transmitting data
  every second as long as the request pin is high.
* Optionally, a header can be added for connecting an I2C OLED display.

