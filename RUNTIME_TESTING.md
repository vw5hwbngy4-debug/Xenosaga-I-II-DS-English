# Runtime QA — English v1.0 Final

This document records the runtime validation status of the final public English release of **Xenosaga I+II for Nintendo DS**.

## Final runtime status

`BOOT_TEST = PASS`

`TITLE_MENU_TEST = PASS`

`NEW_GAME_TEST = PASS`

`OPENING_DIALOGUE_TEST = PASS`

`OPENING_YES_TUTORIAL_ROUTE = PASS`

`TUTORIAL_REFRESHER_TEST = PASS`

`FIRST_BATTLE_TEST = PASS`

`BATTLE_P_E_DISPLAY = PASS`

`CHAPTER_TITLE_PRESENTATION = PASS`

`TEXT_WRAP_READABILITY = PASS`

## Tested route

The final v1.0 candidate was user-tested through:

- cold boot
- title/menu
- New Game
- opening dialogue
- YES warm-up/tutorial route
- tutorial/refresher progression
- first battle
- battle type glyph display
- chapter/title presentation
- general dialogue wrapping and readability

No known visible blocker remained in this tested coverage.

## Previously fixed runtime defects

### Opening YES tutorial freeze

Earlier builds could freeze after choosing **Yes** for the opening warm-up/tutorial.

The issue was traced to stale absolute EVC branch targets after variable-length English text changed event byte offsets.

The supported branch targets were relocated correctly, and the repaired route was runtime-tested successfully.

`YES_BRANCH_RUNTIME_FIX = PASS`

### Dialogue wrapping

Earlier builds could produce awkward inside-word wrapping and isolated fragments.

A whole-game dialogue reflow/wrapping pass was completed before v1.0.

`WHOLE_GAME_WRAP_CLEANUP = PASS`

### Chapter/title graphics

Earlier technical candidates contained corrupted chapter/title graphics.

The final title-card graphics were rebuilt using the corrected safe compression path and runtime-tested successfully.

`CHAPTER_TITLE_GRAPHICS = PASS`

### Battle type display

The final battle UI displays:

- `P` = Physical
- `E` = Ether

`BATTLE_TYPE_GLYPHS = PASS`

## Static verification accompanying runtime QA

The final build also passed the relevant static audits:

- normal player-facing EVC Japanese remaining: **0**
- KJM/title Japanese remaining: **0**
- deep player-facing EVC Japanese remaining: **0**
- BDY Japanese runs remaining: **0**
- item-description Japanese remaining: **0**
- BPS reapplication reproduced the final ROM byte-for-byte

## Intentional non-player-facing residue

Thirteen Japanese `0x4D` fields remain intentionally because they were classified as internal/SFX-style cues rather than normal player-facing text.

Japanese developer/configuration comments also remain in:

- `0/param00.txt`
- `0/param01.txt`
- `0/param02.txt`

These are not normal player-facing game text.

## QA scope

The final release has real runtime testing and extensive static verification.

This does **not** claim an exhaustive every-state or full start-to-finish certification of the complete game.

The correct public description is:

**No known visible issues in tested coverage. Runtime-tested through the opening YES tutorial path and first battle.**

## Final hashes

Clean Japanese source SHA-256:

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

Final English v1.0 BPS SHA-256:

`d0188e2abf13ba81496ec0e387ad3eba3180c7b65af61c2a0dbac96efa71919e`

Expected patched ROM SHA-256:

`5cfe164aea57174ad47801e90f7fd53dccca4d30db2680991d54ec232aac4a61`
