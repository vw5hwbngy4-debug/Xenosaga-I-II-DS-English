# Runtime video evidence

## Public video

**Xenosaga I+II DS in English – Full-Game Rough Translation RC1 Gameplay**  
https://youtu.be/WXCLkwqY2JU

This public gameplay recording shows the current v0.1 RC1 running in English. It provides direct runtime evidence that the build boots and renders English game content outside static extraction/rebuild tests.

### Demonstrated / observed in the current QA session

- gameplay boots and runs;
- English dialogue renders in the opening sequence;
- English speaker labels render;
- the repaired `Yes / No` choice path runs without the previous hard freeze;
- the `No` path also continues normally;
- the word-boundary wrapping repair removes the previously observed isolated one-letter lines in the tested opening sequence;
- menu/status and battle footage are shown during the wider QA recording.

### Issues visible or reported during the same runtime session

- some incoming-mail / notification UI can still contain Japanese text;
- some English font/UI text on the lower screen is difficult to read;
- battle controls/attack behavior have not yet been formally certified by the tester;
- a complete start-to-finish playthrough has not yet been performed.

The video is evidence of a functioning public-QA build, not proof that every scene, battle, side system, or graphical label has been validated.

## Build identity

BPS SHA-256:

`8864d3e9035b92c55148da9870b531f4387defa8153b3d274fbac3469acad464`

Expected patched target SHA-256:

`67c0fe831083ccfe2da21768fecafd31fb68b7e809964157d175147b3f3f1db1`
