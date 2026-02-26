# NLoadingRates.csv

## Overview
- Data from urine collection trials on Welsh Mountain ewes conducted in 2016.
- Six replicate sheep ( labelled 1–6 ) housed in urine collection apparatus.
- Diets: semi-improved pasture (spring, summer, autumn) and improved pasture (autumn).
- Dataset provides: urine event volumes, urine N content per event, estimated urine patch area, N deposited per patch, and resulting nitrogen loading rate for each theoretical urine patch.

## Dataset contents and structure
- File: NLoadingRates.csv
- Data describe individual urine events and associated patch-level nitrogen metrics.
- PatchArea is a calculated hypothetical urine patch area (ha) based on pre-determined wetted area values.
- Wetted area references:
  - 17.5 L urine m-2 for semi-improved pasture patches
  - 8.9 L urine m-2 for improved pasture patches
- Key fields and units:
  - Sheep_No: replicate sheep number (1–6)
  - Season: season data were collected
  - Site: pasture type (semi-improved or improved)
  - N: urine N content (g N L-1)
  - Vol: urine volume (L)
  - PatchArea: hypothetical urine patch area (ha)
  - N_per_patch: nitrogen deposited per urine patch (kg)
  - N_LoadingRate: nitrogen loading rate within each urine patch (kg N ha-1)

## Experimental design and scope
- Six replicate sheep (1–6) in urine collection systems.
- Trials span multiple seasons (spring, summer, autumn) and two pasture types (semi-improved and improved).
- Focus on estimating nitrogen deposition and loading per urine patch, enabling calculation of N loading rates.

## Provenance and authorship
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Usage note: If data are reused please ensure it is fully cited.

## Reuse, citation and governance notes
- Data should be cited with full attribution to the project and authors.
- Metadata describes variables, units, and collection context to support proper data reuse and interoperability.

## Data quality and caveats
- PatchArea is a theoretical calculation based on predetermined site-specific wetted areas, which may affect the interpretation of absolute patch sizes.
- Data represent urine-event level measurements linked to theoretical patch areas and calculated N loading rates, requiring careful alignment between event-level data (N, Vol) and patch-level calculations (N_per_patch, N_LoadingRate).
- Temporal and dietary factors (Season, Site) influence the measurements; users should consider these when aggregating or comparing across conditions.