# Decoder Project

Personal IR **receiver / decoder** build by **Todd Davis** ([Cull3411](https://github.com/Cull3411)).

This repo documents the decoder side of the same Grok-assisted work as [Transponder-Project](https://github.com/Cull3411/Transponder-Project): receive the IR burst, recover timing, and identify the transponder ID.

## Pair project

| Repo | Role |
| --- | --- |
| [Transponder-Project](https://github.com/Cull3411/Transponder-Project) | ATtiny85 Digispark emitter (ID 1 sketch on P1 / PB1) |
| **Decoder-Project** (this repo) | Receiver / decoder that reads that IR and reports an ID |

## What this is

- Hardware + firmware notes for an IR receiver/decoder used with the lap-style transponder
- AI (Grok, ChatGPT, Copilot) used to draft timing and decode logic, then verified on the bench
- Not an unattended AI agent and not a commercial product

## Status

Scaffold created 24 Sep 2026. Add the real decoder sketch and pin-out when you paste them here (same process as the transponder repo).

## Layout

```
firmware/     Arduino / MCU sketches
docs/         AI workflow, hardware notes, decode notes
hardware/     Photos and wiring (upload via GitHub web UI)
```

## How AI was used

Same pattern as the transponder work:

1. State the constraint (board, IR demodulator pin, expected bit time).
2. Ask for a small piece (ISR, gap measurement, ID table) — not the whole system.
3. Treat the reply as a draft.
4. Test against a known-good emitter (Transponder ID 1).
5. Feed back real symptoms ("ID 1 never locks", "gaps read 8 ms not 12.5 ms").

See [docs/ai-workflow.md](docs/ai-workflow.md).

## Author

Todd Davis  
LinkedIn: [linkedin.com/in/todd-davis-4b5b7b37](https://linkedin.com/in/todd-davis-4b5b7b37)
