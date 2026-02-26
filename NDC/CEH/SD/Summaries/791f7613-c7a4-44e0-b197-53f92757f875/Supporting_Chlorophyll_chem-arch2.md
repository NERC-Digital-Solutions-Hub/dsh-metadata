# Supporting information

## Overview
- Describes chemical analysis for chlorophyll a as an overall indicator of phytoplankton biomass.
- Sampling in 2016: water collected at metre intervals from 1 m to 10 m; plus inflows and outflow.
- Sampling in 2017: 0.5 m interval then 1 m to 9 m; lake studied at Blelham Tarn with a monitoring buoy at the deepest point; additional samples at three inflows and the outflow.

## Methods
- Sample collection: 500 mL for the lake, 1000 mL for streams.
- Filtration and preservation: samples filtered immediately after collection through GF/C filter paper (5.5 cm diameter); filter papers frozen; analysed within a month.
- Laboratory analysis: chlorophyll a extracted with methanol and quantified by spectrophotometry.
  - Spectrophotometer settings: 750 nm for background turbidity; 665 nm for chlorophyll a peak.
  - Corrected absorbance Acorr665 = A665 − A750.
- Calculation: Chlorophyll a concentration = (13.9 × Acorr665 × 1/d) × (v/V)
  - 13.9 approximates the reciprocal of the specific absorption coefficient at 665 nm for chlorophyll a in this solvent.
  - d = cuvette path-length (cm); V = volume of sample filtered (mL); v = volume of extract (mL).
- Data outputs: Chlorophyll a concentration in µg/L.

## Data structure
- Date (dd/mm/yyyy)
- Depth (m): coded as -1 (surface) to -10 (deepest) for each measurement
- Chlorophyll a (µg/L)

## Study area context
- Blelham Tarn located in the Lake District, NW England.
- Monitoring buoy located at the deepest point in the lake (around 14.5 m) per Ramsbottom 1976.

## References
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association, Kendal.
- Talling, J.F. (1974) Photosynthetic pigments. In A Manual on Methods for Measuring Primary Productivity in Aquatic Environments, pp. 22–26. Blackwell Scientific Publications.