# esphome-FilHumClimate
ESPHome Filament Dryer Dehumidifier Thermostat Climate control

Hi, this is a project for controlling heater and fan element for drying fillaments for 3D printer. 

For now, switching between climate modes and temperature control is done by HomeAssistant. 

Used Hardware:
- ESP 8266
- DHT22 Temperature & Humidity Sensor
- SH1106 96x16 I2C Display
- WS2812 Addressable LEDs
- Relays
- Air Food Dehydratator (part with fan and heating element)

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
| Name | Mode | Target |
| --- | --- | --- |
| Dry | HEAT | 45°C-50°C |
| Cool-FO | FAN_ONLY | 15°C-35°C |
| Cool | COOL | 15°C-35°C |
| Idle | OFF | 10°C-25°C |

(I want to play with more with cool and fan_only difference and see in future what is better)

Target Humidity should be below 10%.
If reached, climate control is automatically set to cool-fo but there should be some more decidement on previous state of climate control or something.

This whole thing has 2 outputs, for fan and heater.
It is supposed to control relays and switch Fan and Heating element in Air Food Dehydratator.
Working with devices that use high voltage is dangerous.
Please consider your safety, knowledge and skills.
Do it only at your own risk. 
