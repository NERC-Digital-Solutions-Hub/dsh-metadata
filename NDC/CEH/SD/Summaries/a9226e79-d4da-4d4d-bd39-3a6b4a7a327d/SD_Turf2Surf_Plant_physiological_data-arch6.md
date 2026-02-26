# This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf' Details of data structure for the dataset Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016) as detailed in the table Turf2Surf_Plant_physiological_data.csv

## Overview
- Supplements the data series documentation and describes the data structure for plant physiological measurements across North Wales and Northwest England (years: 2013, 2014, 2016).
- Focuses on the Turf2Surf_Plant_physiological_data.csv dataset and its relation to other Turf2Surf datasets.

## Shared data structure (first 9 columns)
- Datasets share the same initial 9 columns:
  - A: Site Number
  - B: Habitat
  - C: Habitat Description
  - D: Site name
  - E: Ecosystem Component (Plant, Soil, or Roots)
  - F: Plant species (if applicable; 'NA' for soil/roots)
  - G: Plot number (1–4)
  - H: Replicate number (used when photosynthesis measurements are not co-located with plots)
  - I: Soil depth interval (for soil/roots)
- Missing values are denoted as NA.
- The 9 shared columns are followed by 9 additional columns, yielding 96 rows in this dataset variant.

## Additional columns (J–R) and their meanings
- J: Year of measurement
- K: Vcmax — Maximum rate of carboxylation at 25 °C (µmol m^-2 s^-1)
- L: Jmax — Electron transport capacity at 25 °C (µmol m^-2 s^-1)
- M: Asat — Photosynthetic rate at saturating irradiance and 400 ppm CO2 at 25 °C (µmol m^-2 s^-1)
- N: Leaf Mass Area — leaf mass per leaf area (gm^-2)
- O: Foliar nitrogen content (%)
- P: Foliar phosphorus content (%)
- Q: Specific leaf area (cm^2 g^-1)
- R: Comments (qualitative notes; none for units)

## Data notes and special cases
- NA indicates measurements not performed for that site.
- At sites 5, 7, 14, and 19, leaves were sampled in 2015 for re-analysis of foliar N and P only.

## Practical implications for data use
- The consistent first-9-column structure enables straightforward merging with the related datasets listed (e.g., plant structural measurements, biomass, and soil datasets for Conwy catchment and surrounding areas).
- Units and descriptions are provided for all measured variables, aiding correct interpretation and unit-aware analyses.
- Handle NA values appropriately during analysis; be aware of year-specific measurements (2013, 2014, 2016) and the 2015 foliar re-analysis notes for certain sites.