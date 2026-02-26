# NLoadingRates.csv

- Project: Uplands-N2O; Grant NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Data reuse note: If data are reused please ensure it is fully cited

## Overview
- Data from urine collection trials conducted in 2016 on Welsh Mountain ewes
- Six replicate sheep (labeled 1–6) housed in urine collection apparatus
- Diets/pastures: semi-improved pasture (spring, summer, autumn) and improved pasture (autumn)

## What the data contain
- Individual urine event records with:
  - Urine volume (Vol) in liters
  - Urine nitrogen content (N) in g N L-1
  - Calculated hypothetical urine patch area (PatchArea) in hectares, based on predetermined site-specific wetted areas
  - Nitrogen deposited in each urine patch (N_per_patch) in kilograms
  - Nitrogen loading rate within each theoretical urine patch (N_LoadingRate) in kg N ha-1
- PatchArea derivation: based on site-specific wetted areas described as 17.5 L urine m-2 for semi-improved pasture patches and 8.9 L urine m-2 for improved pasture patches

## Data structure and headers
- Sheep_No: replicate sheep number
- Season: season data were collected in
- Site: diet/pasture type (semi-improved or improved)
- N: urine N content (g N L-1)
- Vol: urine volume (L)
- PatchArea: hypothetical patch area (ha)
- N_per_patch: N deposited per patch (kg)
- N_LoadingRate: N loading rate per patch (kg N ha-1)

## Experimental design context
- Six sheep analyzed across seasons with two pasture/diet treatments
- Urine patches are theoretical estimates used to compute N deposition and loading rates

## Usage notes and provenance
- Data intended to quantify relationships between urine characteristics, patch areas, and nitrogen loading
- Full citation required if reused
- Data are derived from controlled trials and are suitable for analyses linking urine N concentration, volume, and resulting N loading rates across different pasture types and seasons