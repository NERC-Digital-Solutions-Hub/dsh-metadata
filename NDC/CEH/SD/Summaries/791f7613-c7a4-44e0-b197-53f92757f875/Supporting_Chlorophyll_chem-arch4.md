# Supporting information

## Overview
- Chemical analysis for chlorophyll a as an indicator of phytoplankton biomass.
- Dataset BLEL_Chlorophyll_chem.csv collected for project NEC05744 by Emma Gray.
- Sampling location: Blelham Tarn (Lake District); monitoring buoy at the deepest point (14.5 m).

## Sampling design and collection
- Sample types and volumes:
  - Lake water: 500 mL per sample.
  - Streams: 1000 mL per sample.
- Depths:
  - 2016: samples at depths from 1 m to 10 m (1 m intervals).
  - 2017: samples at 0.5 m, then 1 m to 9 m.
- Additional samples: taken at three inflows and the outflow.
- Sampling times are aligned with monitoring station activities (Fig. 1 indicates buoy location).

## Laboratory analysis and processing
- Filtration: samples filtered immediately after collection using GF/C filter paper (5.5 cm diameter); filters frozen until analysis.
- Analysis window: within one month of collection.
- Pigment extraction and measurement:
  - Chlorophyll a extracted with methanol.
  - Color measured with a spectrophotometer.
  - Background turbidity correction: absorbance at 750 nm (A750).
  - Chlorophyll a measurement wavelength: 665 nm (A665).
- Calculation:
  - Chlorophyll a concentration = (13.9 × A_corr665 × 1/d) × (v/V)
    - A_corr665 = A665 − A750
    - d = cuvette path-length (cm)
    - V = volume of sample filtered (mL)
    - v = volume of extract (mL)
  - The coefficient 13.9 reflects the reciprocal of the specific absorption coefficient at 665 nm for chlorophyll a in this solvent.

## Data structure
- Columns:
  - Date (dd/mm/yyyy)
  - Depth (m): -1 (surface) to -10 (deepest)
  - Chlorophyll a (µg/L)

## Context and references
- Location context: Blelham Tarn mapping and buoy position (deepest point) described; figure referenced (Fig. 1).
- References for methods:
  - Ramsbottom, A. (1976). Depth charts of the Cumbrian lakes.
  - Talling J.F. (1974). Photosynthetic pigments. In A Manual on Methods for Measuring Primary Productivity in Aquatic Environments.
  - Method details cited from Vol- lenweider et al. manual.