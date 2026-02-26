# NLoadingRates.csv

## Overview
- Data from urine collection trials with Welsh Mountain ewes conducted in 2016 (Project: Uplands-N2O, NE/M015351/1).
- Six replicate sheep housed in urine collection apparatus; animals fed either semi-improved pasture (spring, summer, autumn) or improved pasture (autumn).
- Dataset captures all urine events and related nitrogen deposition metrics.

## Data content and structure
- Per-urine-event measurements are provided, including:
  - Urine event volume and nitrogen content per event
  - Estimated urine patch area based on predetermined wetted-area values
  - Nitrogen deposited per urine patch
  - Nitrogen loading rate within each urine patch
- Data is organized at the event level for each of the six sheep across seasons and diets.

## Variables and units
- Sheep_No: replicate sheep identifier (1–6)
- Season: season data were collected
- Site: diet/pasture type (semi-improved or improved)
- N: urine N content (g N L-1)
- Vol: urine volume (L)
- PatchArea: calculated patch area (ha)
- N_per_patch: N deposited per patch (kg)
- N_LoadingRate: N loading rate per patch (kg N ha-1)

## Study context
- Urine patches and nitrogen loading were analyzed using fixed wetted-area assumptions:
  - Semi-improved pasture: 17.5 L urine per m^2
  - Improved pasture: 8.9 L urine per m^2
- PatchArea is reported in hectares, reflecting these site-specific assumptions.
- The dataset provides both per-event data and derived patch-level metrics (N_per_patch, N_LoadingRate).

## Data management and reuse
- Fully cite the dataset if data are reused.
- Data headers and units are explicitly defined to support integration and comparability.
- Authors: Karina A Marsden et al.; Publication context within the Uplands-N2O project.