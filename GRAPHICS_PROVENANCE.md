# Graphics / font provenance status

The current tested build includes a graphics/font engineering pass covering the 18 assets identified through comparison with the public Vector beta.

The beta was used as **technical reference evidence** for changed tiles, layouts, font behavior and asset discovery. The current pass should therefore be treated as **reference-derived engineering output**, not yet as the final provenance-clean graphics implementation.

Before the project calls the graphics layer final, the intended cleanup is:

1. Decode the original Japanese graphic/tile assets.
2. Re-rasterize required English labels independently.
3. Rebuild tile/tilemap/palette data from the Japanese source assets plus our own English raster data.
4. Re-extract and compare the new build.
5. Remove reliance on reference-derived changed tile payloads.

This limitation does not invalidate the independently built EVC translation/runtime work, but it is deliberately disclosed for the public-QA RC1.
