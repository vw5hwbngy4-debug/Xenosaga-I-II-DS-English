# Xenosaga I+II DS — Complete English Translation v1.0

**Status: FINAL PUBLIC RELEASE**

This project is a complete English fan localization of **Xenosaga I+II for Nintendo DS**.

The earlier `v0.1-rc1` release served as the public QA baseline. The project has since undergone additional translation completion, graphics reconstruction, text reflow, database localization, residue auditing and runtime testing.

## Download

### Latest release

**Xenosaga I+II DS – Complete English Translation v1.0**

https://github.com/vw5hwbngy4-debug/Xenosaga-I-II-DS-English/releases/tag/v1.0

The release contains:

- `Xenosaga_I_II_DS_English_v1.0.bps`
- release documentation
- hashes and technical records

No Nintendo DS ROM is distributed.

## Official website

https://xenosaga.wolken.page/

The website includes a local browser patcher.

Dutch localization:

https://xenosaga-nederlands.wolken.page/

## Final v1.0 status

### Translation

- Normal player-facing EVC Japanese remaining: **0**
- KJM / title Japanese remaining: **0**
- Deep player-facing EVC Japanese remaining: **0**
- BDY Japanese runs: **0**
- Item-description Japanese remaining: **0**
- Choice layer translated
- Chapter/title cards translated
- Battle UI localized
- Item descriptions translated
- Whole-game dialogue wrap cleanup completed

Thirteen Japanese `0x4D` fields remain intentionally because they are internal/SFX-style cues rather than normal player-facing text.

Japanese comments also remain in:

- `0/param00.txt`
- `0/param01.txt`
- `0/param02.txt`

These are developer/configuration comments and are not normal player-facing game text.

## Runtime QA

Final v1.0 was tested successfully through:

- cold boot
- New Game
- opening dialogue
- YES warm-up/tutorial route
- tutorial/refresher progression
- first battle
- chapter/title presentation
- battle type display
- general text wrapping/readability

The battle UI now displays:

- `P` = Physical
- `E` = Ether

No known visible blocker remains in the tested coverage.

This is **not** a claim of exhaustive every-state or full-game certification.

## Major fixes since RC1

The final release includes fixes and improvements beyond the original public RC1, including:

- opening YES tutorial freeze fix
- branch relocation fixes
- whole-game dialogue reflow
- deep EVC translation completion
- chapter/title-card graphics reconstruction
- safe graphics compression
- battle P/E sprite glyph replacement
- item database completion
- player-facing Japanese residue cleanup
- final text polish
- reproducible BPS build verification

## Required source ROM

Clean Japanese **Xenosaga I+II** Nintendo DS ROM.

SHA-256:

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

## Final BPS SHA-256

`d0188e2abf13ba81496ec0e387ad3eba3180c7b65af61c2a0dbac96efa71919e`

## Expected patched ROM SHA-256

`5cfe164aea57174ad47801e90f7fd53dccca4d30db2680991d54ec232aac4a61`

## Historical releases

`v0.1-rc1` remains available as the historical public QA release.

It is superseded by **v1.0 Final** and should not be used for a new installation.

## ROM policy

No original or patched commercial ROM is included or distributed.

Users must supply their own supported Japanese copy and apply the BPS patch locally.
