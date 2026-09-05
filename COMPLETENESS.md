# Completeness — English v1.0 Final

This document records the completion status of the final public English localization of **Xenosaga I+II for Nintendo DS**.

## Final status

`ENGLISH_V1_FINAL = PASS`

`SUPPORTED_PLAYER_FACING_TEXT_COMPLETE = PASS`

`BPS_ROUNDTRIP = PASS`

The final release supersedes the earlier `v0.1-rc1` public QA build.

## Translation coverage

### EVC / dialogue

- Supported EVC translatable records: **29,461**
- Normal player-facing EVC Japanese remaining: **0**
- Deep player-facing EVC Japanese remaining: **0**
- KJM/title Japanese remaining: **0**

### Choices

- Choice options translated: **1,286**
- Supported choice-layer Japanese remaining: **0**

### Database / other text

- Item descriptions translated
- Item-description Japanese remaining: **0**
- BDY Japanese runs remaining: **0**
- Speaker labels and supported runtime text integrated

## Graphics and UI

Final v1.0 includes:

- English chapter/title cards
- reconstructed title graphics
- battle type glyph localization
- `P` = Physical
- `E` = Ether
- title/menu/options/status fixes
- graphics residue cleanup in the audited player-facing targets

The chapter/title graphics use the corrected safe compression path and were runtime-tested in the final candidate.

## Text layout

The final build includes a whole-game dialogue wrapping/reflow pass.

The earlier RC1 wrapping defects, including inside-word breaks and isolated fragments observed during runtime testing, were addressed before v1.0.

## Runtime-tested coverage

Final v1.0 was user-tested successfully through:

- cold boot
- title/menu
- New Game
- opening dialogue
- YES warm-up/tutorial route
- tutorial/refresher
- first battle
- battle P/E display
- chapter/title presentation
- general text wrapping/readability

No known visible blocker remained in this tested coverage.

## Intentional non-player-facing Japanese

Thirteen Japanese `0x4D` fields remain intentionally.

These were classified as internal/SFX-style cues rather than normal player-facing dialogue.

Japanese developer/configuration comments also remain in:

- `0/param00.txt`
- `0/param01.txt`
- `0/param02.txt`

These are not normal player-facing game text and are not localization residue presented to the player.

## Verification

Final BPS reapplication to the clean Japanese source reproduced the final English ROM byte-for-byte.

Clean Japanese source SHA-256:

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

Final English v1.0 BPS SHA-256:

`d0188e2abf13ba81496ec0e387ad3eba3180c7b65af61c2a0dbac96efa71919e`

Expected patched ROM SHA-256:

`5cfe164aea57174ad47801e90f7fd53dccca4d30db2680991d54ec232aac4a61`

## QA scope

The final release has substantial static verification and real runtime testing.

It should not be interpreted as a formal exhaustive certification of every possible game state, optional path, save state, menu combination or full start-to-finish playthrough.

The appropriate public description is:

**No known visible issues in tested coverage. Runtime-tested through the opening YES tutorial path and first battle.**
