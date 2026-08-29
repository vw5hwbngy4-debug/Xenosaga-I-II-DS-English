# Known issues / open QA

## 1. Japanese mail / notification UI can still appear

A runtime test confirmed that some Japanese text may still appear when receiving mail. The underlying translated content systems can be English while this separate notification/UI layer remains Japanese.

This is a **confirmed visible-Japanese residue** and should not be hidden behind a blanket “zero visible Japanese everywhere” claim.

Current impact: **not known to block progression**.

## 2. Lower-screen English font can be difficult to read

Some English text on the lower screen is functional but visually hard to read. Font/graphics cleanup is still planned.

Current impact: **readability/polish issue, not currently known to block progression**.

## 3. Battle controls / attack flow are not yet formally certified

The game reaches battle and battle footage exists, but the tester found the keyboard control mapping confusing and did not formally certify attack/command behavior.

Current impact: **QA incomplete**, not a confirmed game logic failure.

## 4. Full playthrough validation is not complete

The opening and early runtime paths have real user confirmation, but the complete game has not yet been validated from start to finish. Additional late-game choice, event, UI, battle, save/load, and graphical-text defects may still surface.

## 5. Typography remains rough

Runtime Fix 1 fixes the observed one-letter/inside-word wrapping regressions using a conservative 36-character word-boundary fallback. Other textbox types may require different pixel-width fitting rules.

## 6. Graphics/font provenance is not final

The current tested graphical pass is reference-derived engineering output based on Japanese-versus-Vector-beta differential analysis. A stricter independent raster/tile rebuild is still planned before calling the graphics layer provenance-clean.

## Reporting bugs

If you find a freeze, untranslated UI, unreadable font, or broken battle/menu behavior, include:

- exact scene/menu;
- emulator or real hardware setup;
- inputs immediately before the issue;
- screenshot or short video if possible;
- whether restarting reproduces it.
