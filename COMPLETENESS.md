# Completeness

This project separates **text-corpus completeness**, **visible UI/graphics completeness**, and **runtime/playthrough validation**. They are not the same gate.

## Passed / machine verified

- Whole supported rough-English machine-readable text layer
- 29,461 supported visible EVC records translated in the text-complete checkpoint
- EVC `0x86` Japanese residue: 0 in the current supported build
- EVC choice layer discovered and rebuilt
- 459 choice blocks / 1,286 Japanese choice options handled
- 1,304 EVC branch targets relocated
- Branch pointer unresolved count: 0
- Naive post-build Japanese `0x02` / `0x86` residue in Runtime Fix 1: 0 / 0
- Max fallback dialogue line length: 36 display characters
- One-letter emitted lines: 0
- NitroFS/FAT/header validation: PASS
- BPS reapply byte-identical: PASS

## Passed / user runtime tested

- Boot to gameplay
- Early English dialogue rendering
- English speaker labels visible in opening scene
- `Yes / No` opening choice
- `Yes` tutorial/Target Drone branch no longer freezes
- `No` branch continues normally
- Opening word-wrap regression fixed
- Continued English gameplay after the opening choice

Public runtime video:

https://youtu.be/WXCLkwqY2JU

## Confirmed residual / incomplete layers

- Some Japanese mail/notification UI remains visible in runtime
- Lower-screen English font readability is rough
- Battle scene is reached, but attack/command control behavior is not yet formally certified
- Full menu/status/battle visual sweep is incomplete
- Late-game runtime proof on the current RC1 is incomplete
- Full playthrough validation is incomplete
- Final independent graphics/font provenance rebuild is incomplete
- Literary editing/polish is incomplete

## Current interpretation

`WHOLE_TEXT_ROUGH_COMPLETE = PASS` refers to the supported machine-readable text corpus and rebuilt text systems.

It does **not** mean that every graphical/UI pixel in the ROM is English. Runtime QA has now confirmed at least one remaining Japanese notification/UI layer.
