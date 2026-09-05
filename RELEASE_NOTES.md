# Xenosaga I+II DS — Complete English Translation v1.0

This is the final public English localization release of **Xenosaga I+II for Nintendo DS**.

The earlier `v0.1-rc1` release was a public QA build. Since then, the project has received additional translation completion, deep-script cleanup, graphics reconstruction, item/database localization, text reflow, residue auditing and runtime testing.

## Final release

GitHub release:

https://github.com/vw5hwbngy4-debug/Xenosaga-I-II-DS-English/releases/tag/v1.0

Official website:

https://xenosaga.wolken.page/

## Final v1.0 highlights

- Complete supported English story/dialogue coverage
- 1,286 translated choice options
- Opening YES tutorial freeze fixed
- EVC branch relocation fixes integrated
- Whole-game dialogue wrap cleanup
- Deep player-facing EVC translation completed
- Chapter/title-card graphics rebuilt in English
- Battle type glyphs localized to `P` and `E`
- Item descriptions translated
- Player-facing Japanese residue removed from the audited supported layers
- BPS reapply verified byte-identical

## Final residue audit

- Normal player-facing EVC Japanese: **0**
- KJM/title Japanese: **0**
- Deep player-facing EVC Japanese: **0**
- BDY Japanese runs: **0**
- Item-description Japanese: **0**

Thirteen Japanese `0x4D` fields remain intentionally because they are internal/SFX-style cues rather than normal player-facing text.

Japanese developer/configuration comments also remain in:

- `0/param00.txt`
- `0/param01.txt`
- `0/param02.txt`

These are not normal player-facing game text.

## Runtime QA

Final v1.0 was user-tested successfully through:

- cold boot
- title/menu
- New Game
- opening dialogue
- YES warm-up/tutorial route
- tutorial/refresher
- first battle
- chapter/title presentation
- battle P/E glyphs
- text wrapping/readability

No known visible issue remained in the tested coverage.

This release does **not** claim an exhaustive every-state or full-game certification.

## Required clean source SHA-256

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

## Final BPS SHA-256

`d0188e2abf13ba81496ec0e387ad3eba3180c7b65af61c2a0dbac96efa71919e`

## Expected patched ROM SHA-256

`5cfe164aea57174ad47801e90f7fd53dccca4d30db2680991d54ec232aac4a61`

No ROM image is included or distributed.
