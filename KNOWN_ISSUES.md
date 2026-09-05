# Known Issues — English v1.0 Final

This document records the known-issue status for the final public English release of **Xenosaga I+II for Nintendo DS**.

## Current status

There are **no known visible blockers in the tested v1.0 coverage**.

The final build was runtime-tested through:

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

The previously reported RC1 issues involving visible Japanese UI residue, rough lower-screen readability, uncertified battle behavior and incomplete graphics cleanup were addressed during the v1.0 work and should not be treated as current known issues.

## Important QA scope

This release has substantial static verification and real runtime testing.

It does **not** claim exhaustive certification of every optional event, every menu state, every save/load path, every late-game branch or a complete start-to-finish playthrough.

The correct interpretation is:

**No known visible issues in tested coverage.**

## Intentional non-player-facing Japanese

Thirteen Japanese `0x4D` fields remain intentionally because they were classified as internal/SFX-style cues rather than normal player-facing text.

Japanese developer/configuration comments also remain in:

- `0/param00.txt`
- `0/param01.txt`
- `0/param02.txt`

These are not normal player-facing localization residue.

## Historical RC1 issues

The following issues were associated with the earlier `v0.1-rc1` QA build and are no longer current v1.0 known issues:

- visible Japanese mail/notification text
- rough lower-screen font/readability
- opening YES tutorial freeze
- incomplete battle command QA
- rough chapter/title graphics
- dialogue wrapping defects
- incomplete deep-script translation
- incomplete item-description localization

## Reporting bugs

If you find a reproducible issue in v1.0, please include:

- exact scene/menu
- emulator or hardware used
- inputs immediately before the issue
- screenshot or short video if possible
- whether restarting reproduces it
- whether the issue occurs on a clean v1.0 patch application

Useful bug categories include:

`FONT_GLYPH`, `FONT_WIDTH`, `TEXT_OVERFLOW`, `LINE_WRAP`, `CHOICE_TEXT`, `BRANCH_FREEZE`, `UNTRANSLATED_UI`, `MENU_LAYOUT`, `GRAPHIC_LABEL`, `PALETTE`, `TILEMAP`, `CONTROL_CODE`, `EVC_RENDER`, `EXECUTABLE_UI`, `DATABASE_UI`, `BATTLE_UI`, `CRASH`, `UNKNOWN`
