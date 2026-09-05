# Patching

## Required source

Use a clean, unmodified Japanese **Xenosaga I+II** Nintendo DS ROM.

Required source SHA-256:

`938d07521cfc937d179402e85c8b0b43f3e929a494838ff1455b29126b56d356`

Game code:

`AXSJ`

## Final patch

Use:

`Xenosaga_I_II_DS_English_v1.0.bps`

Final BPS SHA-256:

`d0188e2abf13ba81496ec0e387ad3eba3180c7b65af61c2a0dbac96efa71919e`

Official release:

https://github.com/vw5hwbngy4-debug/Xenosaga-I-II-DS-English/releases/tag/v1.0

Official website:

https://xenosaga.wolken.page/

## How to apply

Use Floating IPS (FLIPS) or another BPS-compatible patcher.

1. Choose **Apply Patch**.
2. Select `Xenosaga_I_II_DS_English_v1.0.bps`.
3. Select your clean Japanese `.nds` ROM.
4. Save the patched ROM under a new filename.
5. Do not overwrite your clean source ROM.

## Expected patched ROM

Expected final English v1.0 ROM SHA-256:

`5cfe164aea57174ad47801e90f7fd53dccca4d30db2680991d54ec232aac4a61`

A correct patch application should produce this exact hash.

## Verification

The final v1.0 BPS was independently reapplied to the clean Japanese source and reproduced the final English ROM byte-for-byte.

`BPS_ROUNDTRIP = PASS`

## ROM policy

No original or patched Nintendo DS ROM is included in this repository or release.

Users must supply their own legally obtained supported Japanese copy and apply the BPS patch locally.
