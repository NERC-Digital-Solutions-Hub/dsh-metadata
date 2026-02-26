# NLoadingRates.csv

## Overview
- Dataset from urine collection trials on Welsh Mountain ewes conducted in 2016 under the Uplands-N2O project (grant NE/M015351/1).
- Six replicate sheep (labelled 1–6) housed in urine collection apparatus.
- Sheep fed either semi-improved pasture (spring, summer, autumn) or improved pasture (autumn).
- Aims to provide per-urine-event data, estimates of patch-scale nitrogen deposition, and resulting nitrogen loading rates for modelling or policy/research use.

## Data content
- Per-urine-event measurements: urine volume and nitrogen content.
- Patch-scale calculations: hypothetical urine patch area based on predetermined wetted-area assumptions.
- Nitrogen deposition: amount of N deposited per theoretical urine patch.
- Nitrogen loading rate: N loading rate within each theoretical urine patch.

## Experimental design and context
- Diet/pasture: semi-improved vs improved pasture, with season-specific collection data.
- Patch-area calculation: derived from site-specific assumptions:
  - Semi-improved pasture: 17.5 L urine per m²
  - Improved pasture: 8.9 L urine per m²
- Data are organized to enable calculation of N loading at the patch level from individual urine events.

## Variables and units
- Sheep_No: identifier for each replicate sheep.
- Season: season during data collection.
- Site: diet/pasture type (semi-improved or improved).
- N: urine nitrogen content (g N L⁻¹).
- Vol: urine volume (L).
- PatchArea: calculated patch area (hectares, ha).
- N_per_patch: nitrogen deposited per patch (kg).
- N_LoadingRate: nitrogen loading rate per patch (kg N ha⁻¹).

## Reuse and citation
- If data are reused, ensure full citation of the source.
- Data description accompanies the dataset and can be cited in analyses or reports.