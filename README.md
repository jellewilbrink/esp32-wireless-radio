# esp32-wireless-radio
Firmware to transform your ESP32 to a wireless (Bluetooth and WiFi) audio receiver. 

The main goal of this project is to make an ESP32 play webradio and bluetooth audio. To this end, [Edzelf's ESP32Radio-V2](https://github.com/Edzelf/ESP32Radio-V2) is taken as a base and [P. Schatzmann's ESP32-A2DP](https://github.com/pschatzmann/ESP32-A2DP) is added to that. I highly recommend you check out these projects, especially if you only need internet radio or bluetooth, both of which are available under the Apache-2.0 license.
Furthermore, I tweaked the web interface to my personal taste. 

## Setup
### Internal DAC
Although the internal DAC in the ESP32 not suitable for audio, it can be used for an easy debugging setup.

Connect a speaker (e.g. 4 ohm or 8 ohm) in series with a 1 kOhm resistor between GPIO 25 and GND of the ESP32. Make sure to also select the internal DAC as output in the software.

### External DAC
For the wiring I followed this [wiki](https://github.com/pschatzmann/ESP32-A2DP/wiki/External-DAC), in my case for the "Adafuit / UDA1334A Breakout Board":

| DAC |	ESP32       |
|-----|-------------|
| VIN |	5V          |
| GND |	GND         |
| WSEL| WS (GPIO25) |
| DIN |	OUT (GPIO22)|
| BCLK| BCK (GPIO26)|

## Troubleshooting
- If you are on debugging on linux and get an error like "A fatal error occurred: Could not open /dev/ttyUSB0, the port doesn't exist", run `sudo usermod -a -G tty yourname` to add your user to the group that can access the serial ports. 
- On linux you might also need the following for initial setup: https://docs.platformio.org/en/latest/core/installation/udev-rules.html
