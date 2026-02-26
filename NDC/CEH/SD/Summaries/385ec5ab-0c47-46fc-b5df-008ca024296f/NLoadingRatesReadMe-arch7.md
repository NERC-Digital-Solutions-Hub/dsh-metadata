# NLoadingRates.csv

## Overview
- Dataset of urine events from Welsh Mountain ewes collected during 2016 urine trials.
- Six replicate sheep (labeled 1–6) housed in urine collection apparatus.
- Diets: semi-improved pasture (spring, summer, autumn) and improved pasture (autumn).
- Purpose: provide per-event measures and theoretical patch-level nitrogen deposition and loading rates to support map-based analyses.

## Data content and structure
- Fields (headers) and meanings:
  - Sheep_No: identifier for each replicate sheep.
  - Season: season when data were collected (spring, summer, autumn).
  - Site: diet/pasture type (semi-improved or improved).
  - N: urine nitrogen concentration per event (g N L-1).
  - Vol: urine volume per event (L).
  - PatchArea: calculated hypothetical urine patch area (ha), derived from predetermined wetted-area rates.
  - N_per_patch: nitrogen deposited in each urine patch (kg).
  - N_LoadingRate: nitrogen loading rate within each urine patch (kg N ha-1).

## Derived/wetted-area method
- PatchArea is computed using site-specific wetted-area rates:
  - 17.5 L urine per m^2 for semi-improved pasture patches.
  - 8.9 L urine per m^2 for improved pasture patches.

## Spatial and temporal context
- Temporal: data collected across seasons (spring, summer, autumn).
- Spatial context: patches tied to pasture type (semi-improved vs improved) and per-sheep replication.
- Each record relates to an individual urine event and its associated theoretical patch.

## GIS-relevant outputs and usage
- Map-ready metrics:
  - Patch-level N_LoadingRate (kg N ha-1) enables choropleth or symbol-based mapping of nitrogen loading intensity.
  - PatchArea in hectares facilitates generation of patch polygons scaled to area estimates.
- Potential Visualizations:
  - Patch-level maps by Season and Site to compare nitrogen loading across pasture types.
  - Aggregated visuals (e.g., per-sheep, per-season) to assess spatial patterns of N deposition.
- Data integration:
  - Join by Sheep_No, Season, and Site to produce multi-layer visualizations.
  - Combine with field boundary or habitat polygons to contextualize theoretical patches.

## Provenance and citation
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Guidance: If data are reused, ensure full citation.

## Limitations and cautions for GIS use
- PatchArea represents theoretical/wetted-area-based patches, not observed field patch geometries.
- N_per_patch and N_LoadingRate are calculated values based on urine volume, N content, and assumed patch wetted areas; interpretation should consider their derived nature.
- Data reflect 2016 trials with six sheep and specific diets; spatial and temporal extrapolation beyond these conditions should be done cautiously.

## How to acknowledge and reuse
- Attribute the original project and authors.
- Include citation notes as provided and reference the calculated patch-area methodology when presenting spatial products.