SigmaStudio source files for Tesla Model 3 A2B configuration

These files are intended to be used with SigmaStudio for hacking the A2B bus in a
Tesla Model 3 using an AD2428W A2B transceiver, DSP(not implemented yet), and
SigmaLink USBi. Included is a map of the bus architecture, I2C init sequence, and
audio stream configuration.

## How the A2B bus works in a Tesla Model 3:
### The physical bus topology is as follows:
- Car computer -> FOHC mic array -> Rear amplifier
### Stream config:
Master			Slave 0			Slave 1
 _______         _______         _______
|		|  8ch  |		|  8ch  |		|
|  MCU  | ----> | Triple| ----> | Rear  |
|		|  3ch  | Mic   |       | Amp   |
|		| <---- | Array	|       |		|
|_______|       |_______|       |_______|
		B		A		B		A
Contrib 8		Contrib 3		Contrib 0
Consume 3		Consume 0		Consume 8
Pass	0		Pass	8		Pass	0