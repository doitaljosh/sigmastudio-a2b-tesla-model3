SigmaStudio source files for Tesla Model 3 A2B configuration

## Check out my work on getting the amp working with a SigmaDSP here:
[ADAU1452 + A2B Premium amp with DSP processing for tweeters/subwoofer](https://github.com/doitaljosh/tesla-model3-premium-amp-re/tree/experimental/sigma-studio-files/adau1452-ad2410-tesla-amp-upmix)

These files are intended to be used with SigmaStudio for hacking the A2B bus in a
Tesla Model 3 using an AD2428W A2B transceiver, DSP(not implemented yet), and
SigmaLink USBi. Included is a map of the bus architecture, I2C init sequence, and
audio stream configuration.

## How the A2B bus works in a Tesla Model 3:
### The physical bus topology is as follows:
- Car computer -> FOHC mic array -> Rear amplifier
### Stream config:
![Stream Config](https://github.com/doitaljosh/sigmastudio-a2b-tesla-model3/blob/master/stream-config.png?raw=true)
