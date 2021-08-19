# An ESPHome DSMR smart meter reader

An ESPHome smartmeter project (hardware + ESPHome config)

# Compatibility

The device is directly powered by the smart meter. This has been tested with a DSMR v4.2 a DSMR v5.0 meter.

I have a **DSMR v4.2** meter myself, which delivers enough current to power the ESP-01 MCU (100 mA). It does require a 1000 uF capacitor though, to handle the power peak of the ESP-01 during startup and connecting to the WiFi network. I soldered this capacitor at position C7. C1 is empty for me. You can also use two capacitors of around 500 uF and solder these at positions C1 and C7.

A **DSMR v5** meter provides more power (250 mA) and can drive the ESP-01 MCU without additional capacitance. In fact, when using a 1000 uF capacitor, the ESP-01 got stuck in a reboot loop when connecting the device to the smart meter. The device does work with no capacitors at all at positions C1 and C7.

Please let me know if you find additional compatibility outcomes.

![final](final.png)

# Prototype

Before desiging the final board from above, I designed and built a prototype.
Here's what this one looked like:

![prototype](prototype.jpg)

# Credits

The circuit that I used as a starting point for my board:
https://klushok.etv.tudelft.nl/projects/view?id=8
