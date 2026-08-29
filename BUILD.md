# Build / engineering notes

The public patch is produced against the clean Japanese ROM identified in `SOURCE_ROM_HASHES.txt`.

Runtime Fix 1 adds two important pieces of EVC infrastructure:

- choice parsing/rebuilding for `0x23` / repeated `0x24` / `0x25` structures;
- relocation of supported absolute EVC branch targets after variable-length text rebuilds.

The included scripts under `tools/` are engineering evidence from the current workspace. Some build paths in `BUILD_EVIDENCE_ONLY.py` still refer to the original analysis workspace and are **not yet a portable one-command public build**. Do not represent this package as source-complete reproducibility until those workspace dependencies are consolidated.

The BPS itself is verified byte-identical when reapplied to the required clean Japanese source ROM.
