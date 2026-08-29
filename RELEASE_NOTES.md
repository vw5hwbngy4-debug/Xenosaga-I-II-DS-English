# Xenosaga I+II DS Rough English v0.1 RC1

This is a **Public QA release candidate** of a broad rough-English localization. It prioritizes readable English coverage and runtime functionality over polished prose and perfect graphics.

## Runtime video

**Xenosaga I+II DS in English – Full-Game Rough Translation RC1 Gameplay**  
https://youtu.be/WXCLkwqY2JU

## Highlights

- Complete supported machine-readable rough-English text layer.
- Opening gameplay booted and tested successfully.
- Identified and translated the separate Japanese choice layer globally: 1,286 choice options across 459 choice blocks.
- Fixed the opening **Yes** tutorial hard freeze by relocating absolute EVC branch targets after variable-length translation.
- 1,304 branch targets relocated; 0 unresolved in the current static audit.
- Fixed observed one-letter/inside-word line wrapping with a 36-character word-boundary fallback.
- User confirmed both **Yes** and **No** opening paths continue normally.
- Continued English gameplay has been captured publicly on video.

## Known issues

- Some Japanese UI/notification text still appears. A confirmed example is the incoming-mail notification layer.
- Some lower-screen English font/UI text is difficult to read.
- Battle scenes are reached, but attack/command controls are not yet formally smoke-test certified.
- Late-game QA and full start-to-finish playthrough validation are still incomplete.
- The current graphics/font pass is still marked as reference-derived engineering output pending a stricter independent rebuild.

These known issues are not currently known to block progression, but this RC1 should be treated as a public testing build rather than a final localization.

## Required clean source SHA-256

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

## Patch SHA-256

`8864d3e9035b92c55148da9870b531f4387defa8153b3d274fbac3469acad464`

## Expected patched ROM SHA-256

`67c0fe831083ccfe2da21768fecafd31fb68b7e809964157d175147b3f3f1db1`

No ROM image is included.
