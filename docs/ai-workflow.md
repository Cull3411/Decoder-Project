# AI workflow (decoder)

## Pattern

1. Describe the receiver hardware and what a good packet looks like (bit time, repeats, gap).
2. Ask Grok for one function: pulse timing, gap classification, or ID match — not a full product.
3. Verify against a known-good emitter. The published example is [Transponder ID 1](https://github.com/Cull3411/Transponder-Project/blob/main/firmware/Transponder_ID1/Transponder_ID1.ino) — one ID from the set **1–96**.
4. Paste serial logs or measured gaps back into the chat when it fails.

## Known emitter numbers (from the pair project)

- IDs: **1 through 96** (nearly all worked through; ID 1 is the example sketch)
- Block width: `BLOCK_US = 139`
- Message length: 30 bits, repeated `REPETITIONS_PER_MESSAGE` (default 130)
- Inter-message gaps: 24-value array, multiples of 40 µs, average 12 500 µs
- Carrier: ~38 kHz on the emitter (use a 38 kHz IR demodulator on this side)

## What to check before trusting a decode

- Demodulator pin vs sketch pin
- Active-low vs active-high output from the IR receiver module
- Whether you are measuring raw carrier or already-demodulated envelope
- Gap average near 12.5 ms when the example ID 1 emitter is transmitting
