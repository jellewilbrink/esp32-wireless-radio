# Other sources
Before deciding on the feasibility and the libraries to use for this project, some sources were studied.

## Bluetooth audio sink
- https://github.com/pschatzmann/ESP32-A2DP
    - Awesome library worked at first try with only a few lines of code!
    - example of implementation: https://github.com/paulgreg/esp32-bluetooth-audio


## WiFi internet radio / streaming
- https://github.com/pschatzmann/esp32_radio
    - GPL license. I could not get this to work yet. It does feature both a nice webradio player and bluetooth functionality. But no OTA updates.
- https://github.com/Edzelf/ESP32Radio-V2
    -  More permissive license. Seems to work nicely, although I could not yet try audio output. Better documentation and additional features and hardware support. Features nice webradio player and OTA updates (not yet tried though), but no bluetooth streaming.
    -  Suggestion: add bluetooth functionality to this using pschatzmann/ESP32-A2DP
- https://github.com/pisicaverde/yet-another-internet-radio-ESP32
- https://github.com/michelep/ESP32_WebRadio

## ESP32 development
- pinout: https://circuitstate.com/pinouts/doit-esp32-devkit-v1-wifi-development-board-pinout-diagram-and-reference/
