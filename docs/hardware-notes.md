# Hardware notes (decoder)

Fill this in from the Receiver/Decoder Grok project and from photos of the working unit.

## Board

- [ ] MCU / board type:
- [ ] IR receiver module (e.g. TSOP / VS1838 / other):
- [ ] Carrier expected: 38 kHz (matches the Digispark emitter)
- [ ] Power source:

## I/O

| Function | Planned pin | Confirmed on bench |
| --- | --- | --- |
| IR demodulator data | | |
| Status LED | | |
| Serial debug | | |

## Pairing

Test against the working transponder:

- Emitter: Digispark rev3, IR LED on **P1 / PB1 / D1** (`IR_LED_PIN = 1`)
- Emitter power: RC 5 V → Digispark 5V, common GND
- Clone silk may print "P1 D0 PWM" on that pad; it is still PB1

## Photos

Upload decoder photos to `hardware/` using GitHub **Add file → Upload files** (the connector used here cannot push large JPEGs). Then link them in this file.
