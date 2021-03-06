# ledhandler
## Description

This code is intended to react on some Snips events on the mqtt bus and use the Respeaker LEDs accordingly. 
Tested with the ReSpeaker 7-mic Array (not tested with other respeaker boards).

It's freely forked from snispmanagercore and has been adapted to the unique use of managing the LEDs.

Work in progress !

## Features
Current version has the following events and actions :

* Welcome (Led handler starting) : Raising blue light, then switch to standby
* Standby (hotword/toggleOn) : Activate "DOA" mode
* Intent OK (nlu/intentParsed) : Set all LEDs to green (= OK)
* Intent NOK (nlu/intentNotRecognized) : Flashing red LEDs (= error)
* Listening (hotword/#/detected) : Looping rainbow
* Speaking (tts/say) : Switching between colors


It uses some defaults mode whenever possible. For example, setting all the leds to the same colour is done with only one call.

## Support
Tested with:
* Respeaker 7-mic array USB
* Python 3.5


## Requirements:
* Respeaker module (pip3 install respeaker) 
* colour module (pip3 install colour)

## TODO:
- [ ] config file (use /etc/snips.toml ?)
- [ ] add animations/colors in config
- [ ] Implement manual testing of each state

## References: 

snipsmanagercore : https://github.com/snipsco/snipsmanagercore (not really a fork...)

Respeaker Protocol : https://github.com/respeaker/ReSpeaker-Microphone-Array-HID-tool/blob/master/respeaker%20micarray%20hid%20protocol.xlsx

