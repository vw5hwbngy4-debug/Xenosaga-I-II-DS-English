# Changelog

## v0.1-rc1 — Public QA / Runtime Fix 1

- Promoted whole supported machine-readable text layer to rough-English complete.
- Added real EVC choice parsing (`0x23` / `0x24` / `0x25`).
- Translated 1,286 Japanese choice options across 459 choice blocks.
- Added EVC absolute branch relocation for supported `0x26` / `0x27` opcodes.
- Relocated 1,304 branch targets with 0 unresolved pointers in the current audit.
- Fixed the opening `Yes` branch hard freeze.
- Replaced the old 40-byte dialogue fallback with conservative 36-character word-boundary wrapping.
- User confirmed boot, opening English dialogue, `Yes` route, `No` route and the observed wrap regression fix.
- Added public runtime gameplay video: https://youtu.be/WXCLkwqY2JU
- Documented confirmed Japanese residue in the incoming-mail notification/UI layer.
- Documented lower-screen English font readability as a known issue.
- Battle smoke test and full playthrough remain open.
