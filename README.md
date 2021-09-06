SigmaStudio source files for Tesla Model 3 A2B configuration

These files are intended to be used with SigmaStudio for hacking the A2B bus in a
Tesla Model 3 using an AD2428W A2B transceiver, DSP(not implemented yet), and
SigmaLink USBi. Included is a map of the bus architecture, I2C init sequence, and
audio stream configuration.

## How the A2B bus works in a Tesla Model 3:
### The physical bus topology is as follows:
- Car computer -> FOHC mic array -> Rear amplifier
### Stream config:
![Stream Config](https://github.com/doitaljosh/sigmastudio-a2b-tesla-model3/blob/master/stream-config.png?raw=true)