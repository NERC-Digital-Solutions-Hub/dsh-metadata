# BLEL_Chlorophyll_chem.csv

## Overview
- Chemical analysis for chlorophyll a to indicate phytoplankton biomass in Blelham Tarn (NW England).
- Data collected in 2016 and 2017, with sampling at multiple depths (1–10 m in 2016; 0.5 m then 1 m to 9 m in 2017) within the lake and at three inflows and the outflow.
- Monitoring buoy located at the deepest point in the lake (14.5 m) as shown in Figure 1.
- Data structure includes Date, Depth, and Chlorophyll a (µg/L). Collected by Emma Gray for project NEC05744.
- Figure 1 illustrates the lake location and buoy placement; references include Ramsbottom (1976) and Talling (1974).

## Sampling and Handling
- Water sample volumes: 500 mL for the lake, 1000 mL for streams.
- Samples collected at metre intervals in the water column from surface to depth (1–10 m in 2016; 0.5 m then 1 m to 9 m in 2017) and at three inflows/outflow.
- Immediately filtered after sampling using GF/C filter paper (5.5 cm diameter).
- Filter papers frozen; samples analyzed within one month of collection.
- Chlorophyll a extraction performed using methanol; colour measured with a spectrophotometer.

## Analytical Method
- Spectrophotometer readings:
  - 750 nm to correct for background turbidity.
  - 665 nm as the red absorbance maximum for chlorophyll a.
- Corrected absorbance: A_corr665 = A665 − A750.
- Chlorophyll a concentration calculation:
  - Chlorophyll a (µg/L) = (13.9 × A_corr665 × 1/d) × (v/V)
  - 13.9 is the reciprocal of the specific absorption coefficient at 665 nm in this solvent.
  - V = volume of sample filtered (mL); v = volume of extract (mL); d = path-length of cuvette (cm).

## Data Structure
- Date: dd/mm/yyyy.
- Depth: meters, with -1 representing the first measurement from the surface to -10 for the deepest measurement.
- Chlorophyll a: concentration in µg/L.

## Spatial/Temporal Context
- Location: Blelham Tarn, Lake District, NW England.
- Monitoring buoy at the lake’s deepest point (14.5 m); data captured at varying depths to profile phytoplankton biomass over time.
- Data span two years (2016 and 2017) with depth-specific sampling schedules as described.

## References
- Ramsbottom, A. (1976). Depth charts of the Cumbrian lakes. Freshwater Biological Association. Kendal.
- Talling J.F. (1974). Photosynthetic pigments. In: Manual on Methods for Measuring Primary Productivity in Aquatic Environments. Blackwell Scientific Publications, Oxford.