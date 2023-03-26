# Other sources
Before deciding on the feasibility and the libraries to use for this project, some sources were studied.

## Bluetooth audio sink
- https://github.com/pschatzmann/ESP32-A2DP
    - Awesome library worked at first try with only a few lines of code!
    - example of implementation: https://github.com/paulgreg/esp32-bluetooth-audio


## WiFi internet radio / streaming
- https://github.com/pschatzmann/esp32_radio
    - Phil's blog: https://www.pschatzmann.ch/home/2020/04/13/the-most-beautiful-radio-music-player-for-the-esp32/
    - GPL license. I could not get this to work yet. It does feature both a nice webradio player and bluetooth functionality. But no OTA updates.
- https://github.com/Edzelf/ESP32Radio-V2
    -  More permissive license. Seems to work nicely, although I could not yet try audio output. Better documentation and additional features and hardware support. Features nice webradio player and OTA updates (not yet tried though), but no bluetooth streaming.
    -  Suggestion: add bluetooth functionality to this using pschatzmann/ESP32-A2DP
- https://github.com/pisicaverde/yet-another-internet-radio-ESP32
- https://github.com/michelep/ESP32_WebRadio

Package chosen to use: Edzelf/ESP32Radio-V2. pschatzmann/esp32_radio already has all desired features except for OTA, which would be very easy to implement. However, its license is less permissive; I don't know vue, whereas I can easily modify the webinterface by Edzelf to my liking; and the ESP32Radio-V2 offers much more hardware support, something I might use in the future. The flipside is that ESP32Radio-V2, so I will have to add this feature. This is harder than simply setting up ArduinoOTA, but should still be easily doable. Therefore, I choose Edzelf/ESP32Radio-V2 as a basis to which I will integrate pschatzmann/ESP32-A2DP for bluetooth support.
    
Nice api endpoint: https://nl1.api.radio-browser.info/json/stations/bycountrycodeexact/NL?hidebroken=true

## ESP32 development
- pinout: https://circuitstate.com/pinouts/doit-esp32-devkit-v1-wifi-development-board-pinout-diagram-and-reference/
