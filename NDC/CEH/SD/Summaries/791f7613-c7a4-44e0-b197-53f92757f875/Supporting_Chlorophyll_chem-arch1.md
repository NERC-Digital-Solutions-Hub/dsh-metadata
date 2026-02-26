# BLEL_Chlorophyll_chem.csv

## Purpose
- Chemical analysis for chlorophyll a provides an overall indication of phytoplankton biomass.

## Sampling design and procedure
- Water sample volumes: 500 mL for the lake; 1000 mL for the streams.
- Depth sampling: metre intervals from 1 m to 10 m in 2016; 0.5 m then 1 m to 9 m in 2017.
- Additional samples taken at three inflows and the outflow.
- Samples collected at the monitoring buoy located at the deepest point in Blelham Tarn (14.5 m).

## Analytical method
- Filtration: samples filtered immediately after collection using a GF/C filter paper (5.5 cm diameter).
- Preservation: filter paper frozen and analyzed within a month.
- Extraction and measurement: chlorophyll a extracted with methanol and colored measured with a spectrophotometer.
- Spectrophotometer settings: 750 nm for background turbidity (A750) and 665 nm for chlorophyll a (A665).
- Corrected absorbance: A_corr665 = A665 − A750.
- Concentration calculation: Chlorophyll a concentration = (13.9 × A_corr665 × 1/d) × (v/V), where
  - d = cuvette path-length (cm),
  - V = volume of sample filtered (ml),
  - v = volume of extract (ml).

## Data structure
- Columns: Date (dd/mm/yyyy), Depth (m) (from -1 surface to -10 deepest), Chlorophyll a (µg/L).

## Location and figure
- Location: Blelham Tarn, Lake District, Northwest England.
- Figure: monitoring buoy at the deepest point; bathymetry reference from Ramsbottom (1976).

## References
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes, Freshwater Biological Association.
- Talling, J.F. (1974) Photosynthetic pigments. In A Manual on Methods for Measuring Primary Productivity in Aquatic Environments.