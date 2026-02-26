# NLoadingRates.csv

## Overview
- Dataset from the Uplands-N2O project (Grant NE/M015351/1) compiling urine-related nitrogen metrics from Welsh Mountain ewes during 2016 urine collection trials.
- Six replicate sheep were used, housed in urine collection apparatus and fed two pasture types: semi-improved pasture (spring, summer, autumn) and improved pasture (autumn).
- Purpose: provide per-event and per-patch nitrogen data to assess nitrogen loading and related environmental implications.

## Data collection and scope
- Data capture: all urine events for each of the six sheep across seasons and pasture types.
- Diet/pasture distinctions: semi-improved vs. improved pasture, with season-specific collection.
- Key outcome: theoretical nitrogen loading on urine patches derived from individual urine events.

## Data structure and Units
- Data headers and units:
  - Sheep_No: identifier for each replicate sheep
  - Season: season during data collection
  - Site: diet/pasture type (semi-improved or improved)
  - N: urine nitrogen content (g N L-1)
  - Vol: urine volume (L)
  - PatchArea: calculated hypothetical urine patch area (ha) based on predetermined wetted-area rules
  - N_per_patch: nitrogen deposited in each urine patch (kg)
  - N_LoadingRate: nitrogen loading rate within each urine patch (kg N ha-1)

## Key variables and their meaning
- N (g N L-1) and Vol (L): determine total nitrogen excreted per urine event.
- PatchArea (ha): patch footprint derived from fixed urine-wetted-area assumptions (17.5 L per m^2 for semi-improved; 8.9 L per m^2 for improved).
- N_per_patch (kg) and N_LoadingRate (kg N ha-1): quantify spatially explicit nitrogen deposition and intensity per hectare.

## Potential monitoring and policy relevance
- Provides a concrete environmental health metric: patch-scale nitrogen deposition and per-hectare loading rates.
- Useful for evaluating pasture management strategies and their impact on nitrogen loading and potential downstream environmental effects (e.g., leaching, emissions in upland systems).
- Supports calibration and validation of models linking livestock urine to N cycling and N2O emissions in upland pastures.

## Data quality, governance, and reproducibility
- Reuse note: if data are reused, full citation is required.
- Metadata clarity: data headers and units are specified; however, additional methodological metadata (e.g., urine collection apparatus specifics, calibration details) would aid reproducibility and cross-study comparability.
- Data sharing considerations: sharing underlying datasets and metadata is valuable for transparency but may require addressing data governance and access constraints.

## Limitations and considerations for use
- Temporal and spatial scope: data from 2016 Welsh Mountain ewes under controlled urine collection; results may have limited generalizability to other breeds, regions, or management systems.
- Requires careful interpretation of PatchArea calculations and the assumed wetted-area constants to ensure accurate patch-level inferences.
- To maximize monitoring value, accompany with metadata on measurement procedures, calibration, and data processing steps.