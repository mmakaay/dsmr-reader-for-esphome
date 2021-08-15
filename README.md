# An ESPHome DSMR smart meter reader

An ESPHome smartmeter project (hardware + ESPHome config)

# Compatibility

The device is directly powered by my smart meter. I have a DSMR v4.2 meter, which delivers enough current to power the ESP-01 MCU. The device requires the two 1000uF capacitors to handle the power peak of the ESP-01 during startup and connecting to the WiFi network.

DSMR v5 meters should work as well. I don't know about other versions. If you want to use the device with a different DSMR version, then please check the specification of the 5V power supply line of the meter, to see if it's as good or better than the one in my v4.2 meter: it supplies a maximum current of 100 mA at 5 Volt.

![final](final.png)

# Prototype

Before desiging the final board from above, I designed and built a prototype.
Here's what this one looked like:

![prototype](prototype.jpg)

# Credits

The circuit that I used as a starting point for my board:
https://klushok.etv.tudelft.nl/projects/view?id=8
