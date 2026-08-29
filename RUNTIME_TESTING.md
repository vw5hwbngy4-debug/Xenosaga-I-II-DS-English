# Runtime QA

## Public evidence

Gameplay video:

**Xenosaga I+II DS in English – Full-Game Rough Translation RC1 Gameplay**  
https://youtu.be/WXCLkwqY2JU

## Confirmed by user testing

- `BOOT_TEST = PASS`
- `EARLY_DIALOGUE_TEST = PASS`
- `OPENING_YES_NO_CHOICE = PASS`
- `YES_BRANCH_RUNTIME_FIX = PASS`
- `NO_BRANCH_RUNTIME_TEST = PASS`
- `OPENING_WORD_WRAP_FIX = PASS`
- `POST_CHOICE_ENGLISH_GAMEPLAY = PASS`

The original `Yes` freeze was traced to stale absolute branch targets in variable-length translated EVC files. Runtime Fix 1 relocates supported branch operands and the user confirmed that the previously freezing tutorial route now continues.

## Confirmed issues from runtime

- `MAIL_NOTIFICATION_VISIBLE_JAPANESE = PRESENT`
- `LOWER_SCREEN_FONT_READABILITY = ROUGH`
- `BATTLE_SCENE_REACHED = YES`
- `BATTLE_ATTACK_COMMAND_SMOKE_TEST = NOT_YET_CONFIRMED`
- `FULL_PLAYTHROUGH_VALIDATION = NOT_YET_COMPLETE`

## Still needed

- Focused mail/notification text-source audit
- Lower-screen font readability cleanup
- Main menu / Status / Items / Options / Save-Load sweep
- Battle attack/command smoke test with a comfortable DS-style controller mapping
- Additional choice-heavy scenes
- At least one late-game translated event
- Full playthrough

## Bug categories

When reporting a defect, use one of:

`FONT_GLYPH`, `FONT_WIDTH`, `TEXT_OVERFLOW`, `LINE_WRAP`, `CHOICE_TEXT`, `BRANCH_FREEZE`, `MAIL_NOTIFICATION`, `UNTRANSLATED_UI`, `MENU_LAYOUT`, `GRAPHIC_LABEL`, `PALETTE`, `TILEMAP`, `CONTROL_CODE`, `EVC_RENDER`, `EXECUTABLE_UI`, `DATABASE_UI`, `BATTLE_UI`, `CRASH`, `UNKNOWN`.
