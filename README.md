# esphome-FilHumClimate
ESPHome Filament Dryer Dehumidifier Thermostat Climate control

Hi, this is a project for controlling heater and fan element for drying fillaments for 3D printer. 

Used Hardware:
- ESP 8266
- DHT22 Temperature & Humidity Sensor
- SH1106 96x16 I2C Display
- WS2812 Addressable LEDs

I implemented second DHT22 sensor just for logging purposes and future corrections according to box sizes.

States of climate control should be seen on addressable WS2812 LEDs. (For now 10 leds strip)
- Heating - Red pulsing
- Cooling - Blue
- Fan_Only - Azure
- Idle - Rainbow

Temperature and Humidity of both sensors should be seen on SH1106 96x16 I2C Display


| Temp1 | Hum1 |
| ----- | ---- |
| Temp2 | Hum2 |

(Thinking about adding climate state too, but the display is too small)

Climate presets ready to use
- Dry - Mode: heat, Target: 45°C-50°C
- Cool-FO - Mode: fan_only, Target: 15°C-35°C
- Cool - Mode: cool, Target: 15°C-35°C
- Idle - Mode: off, Target: 10°C-25°C

(I want to play with more with cool and fan_only difference and see in future what is better)

Target Humidity should be below 10%.
If reached, climate control is automatically set to cool-fo but there should be some more decidement on previous state of climate control or something.
