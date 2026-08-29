# Xenosaga I+II DS — Rough English v0.1 RC1

**Status: Public QA release candidate. This is not a polished final localization.**

This project is an independently produced rough-English localization of the Nintendo DS version of **Xenosaga I+II**. The priority of this RC1 is broad English readability, reproducible patching, and real runtime testing. Literary editing, final graphics/font cleanup, and full-playthrough certification come later.

## 🎥 Runtime gameplay video

**Xenosaga I+II DS in English – Full-Game Rough Translation RC1 Gameplay**  
https://youtu.be/WXCLkwqY2JU

The video shows the current RC1 running in real gameplay with English dialogue, choices, menus/status screens and battle footage. It is public runtime evidence for the build, not a claim of completed full-game QA.

## Current verified state

- Core/story machine-readable text: **complete rough English**
- Supported visible EVC Japanese remaining: **0**
- EVC choice menus: **1,286 Japanese options found; 0 remaining in the supported choice layer**
- EVC branch relocation: **1,304 targets relocated; 0 unresolved**
- Boot to gameplay: **PASS, user tested**
- Early English dialogue: **PASS, user tested**
- Opening `Yes / No` choice: **PASS, user tested**
- Previously freezing `Yes` tutorial branch: **PASS, user tested after relocation fix**
- `No` branch: **PASS, user tested**
- Opening dialogue word-wrap fix: **PASS, user tested**
- Battle scene: **reached and shown, controls/attack behavior not yet formally certified**
- Full playthrough validation: **not yet complete**

## Known visible issues

This RC1 is playable for public QA, but it is not visually clean everywhere:

- Some Japanese UI/notification text can still appear. A confirmed example is the incoming-mail notification layer.
- Some English text on the lower screen is difficult to read because the current font/graphics treatment is still rough.
- Battle controls have not yet received a formal smoke-test certification.
- Other late-game UI or graphical-text residue may still surface during wider testing.

These issues are **not currently known to block progression**, but a full end-to-end playthrough has not yet been certified.

See [KNOWN_ISSUES.md](KNOWN_ISSUES.md) and [RUNTIME_TESTING.md](RUNTIME_TESTING.md).

## Runtime Fix 1

The first real playtest exposed two major defects:

1. Some English dialogue wrapped inside words and produced isolated one-letter lines.
2. Choosing **Yes** at `Do you want to warm up before the mission?` froze the game.

The wrapping defect is now handled with conservative word-boundary fitting using a 36-character fallback for the current dialogue path.

The freeze was traced to stale absolute EVC branch offsets after variable-length English text shifted later event bytecode. The serializer now relocates supported `0x26` and `0x27` branch targets. The separate EVC choice structure was also identified and translated globally.

The user retested the previously freezing **Yes** route and confirmed it now continues normally.

See `reports/runtime_fix1/runtime_fix1_summary.json` for machine-readable evidence.

## Patch

The patch itself is shipped as a GitHub Release asset rather than a ROM image:

`xenosaga_i_ii_ds_rough_english_v0.1-rc1.bps`

See [PATCHING.md](PATCHING.md).

## What “RC1” means here

RC1 means this rough-English build is ready for wider runtime QA. It does **not** mean:

- final literary editing;
- zero Japanese pixels on every screen;
- perfect lower-screen typography;
- complete battle-system QA;
- full-game playthrough certification;
- final graphics provenance cleanup.

Please report freezes, unreadable text, untranslated UI, battle/control problems, or late-game regressions with screenshots or short video clips. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Graphics / font provenance note

The current user-tested build contains an engineering graphics/font pass reconstructed through Japanese-versus-Vector-beta differential analysis. Vector was used as technical/layout evidence. This graphics layer is still marked as reference-derived engineering output and is scheduled for a stricter independent raster/tile rebuild before a provenance-clean final release.

The translation corpus and EVC runtime fixes are not intended to copy Vector's English prose.

See [GRAPHICS_PROVENANCE.md](GRAPHICS_PROVENANCE.md) and [LICENSES_AND_PROVENANCE.md](LICENSES_AND_PROVENANCE.md).

## ROM policy

No Nintendo DS ROM is included or distributed. You must supply your own legally obtained clean Japanese ROM matching the SHA-256 in `SOURCE_ROM_HASHES.txt`.
