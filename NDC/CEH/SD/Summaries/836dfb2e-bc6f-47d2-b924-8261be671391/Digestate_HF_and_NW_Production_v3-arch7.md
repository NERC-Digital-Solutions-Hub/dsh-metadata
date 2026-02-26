# Digestate_HF_and_NW_Production.csv

## Overview
- Supplement describing the data structure for the Digestate_HF_and_NW_Production.csv dataset.
- Contains 7 columns and 90 rows from a 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Measurements include plant yield, grain yield, and thousand grain weight (TGW) across various digestate and nitrogen treatments.

## Data structure and fields
- Site: HF or NW (location of the trial).
- Plot: experimental plot number.
- Block: blocking factor in a randomized block design (values 1–5).
- Treatment: digestate-related treatments and mineral nitrogen rates.
  - Digestate treatments: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
  - Mineral N rates: N-75, N-150, N-225, N-300 (NH4NO3 at 75, 150, 225, 300 kg N ha-1 respectively).
- Plant_yield: whole plant yield at 100% dry matter (tonnes per hectare).
- Grain_yield: grain yield at 100% dry matter (tonnes per hectare).
- TGW: thousand grain weight at 100% dry matter (grams).
- All yield data reported at 100% dry matter; NA indicates not assessed.

## Spatial context and plot details
- HF (Henfaes) and NW (North Wyke) are the two study sites.
- Plot harvest area varies by site and treatment:
  - HF: 1.2 m x 6.5 m for nitrogen-rate plots; 1.2 m x 14 m for C, D, AD, DNI, ADNI.
  - NW: 2 m x 4.5 m for nitrogen-rate plots; 2 m x 9 m for C, D, AD, DNI, ADNI.
- Differences in plot sizes by site are important for GIS mapping and area calculations.

## Dataset scope
- Year: 2017.
- Location coverage: Henfaes Research Center (HF) and North Wyke (NW), Rothamsted Research collaboration.
- Size: 90 observations (rows) and 7 data columns.

## Considerations for GIS use
- Suitable for map-based visualization of yields by site, treatment, and plot.
- Can be joined with spatial plot boundaries and site-level GIS layers; account for differing plot sizes between HF and NW during area calculations.
- Useful for comparing digestate treatments vs. mineral nitrogen and for analyzing effects of nitrification inhibitors (DMPP).
- Be mindful of NA values where data were not assessed; ensure consistent data standards when integrating with other datasets.