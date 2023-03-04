# esp32-wireless-radio
Firmware to transform your ESP32 to a wireless (Bluetooth and WiFi) audio receiver

## Troubleshooting
- If you are on debugging on linux and get an error like "A fatal error occurred: Could not open /dev/ttyUSB0, the port doesn't exist", run `sudo usermod -a -G tty yourname` to add your user to the group that can access the serial ports. 
- On linux you might also need the following for initial setup: https://docs.platformio.org/en/latest/core/installation/udev-rules.html