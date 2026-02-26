# CEH Land Cover plus: Fertilisers 2010-2015 (England)

## Overview
- Provides maps of predicted average annual application rates for nitrogen (N), phosphorus (P), and potassium (K) fertilisers in England from 2010 to 2015 at 1 km × 1 km resolution, with associated uncertainty.
- Created under the ASSIST project to explore environmental impacts of agrochemical use and support sustainable farming decisions.
- Data are designed for modelling nutrient fate, GHG emissions related to fertiliser use, and assessing ecological and agricultural indicators.

## Data Access and Citation
- Access: Environmental Information Data Centre (EIDC) at https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051
- Required citation: Osório, B.; Redhead, J.W.; Jarvis, S.G.; May, L.; Pywell, R.F. (2019). CEH Land Cover plus: Fertilisers 2010-2015 (England). NERC Environmental Information Data Centre. https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051

## Data Description
- Content: Maps of predicted average annual fertiliser application rates (kg/km2) for N, P, and K, across England, for 2010–2015, plus their uncertainty estimates.
- Data were modelled from Defra’s British Survey of Fertiliser Practice (BSFP) using spatial interpolation.
- Cropping context: Interpolation uses crop typology data derived from Land Cover plus: Crops (Crops) map (2015–17 average) based on Sentinel data.

## Collection Methods
- Raw data source: BSFP, supplied by Defra; yearly surveys (2010–2015) of fertiliser application rates (kg/ha) with georeferenced farm data.
- Survey characteristics: voluntary participation; ~3,696 farms per year; 66 crop classes; includes coordinates, soil type, field counts, and IDs.
- Data handling decisions:
  - Zero values are excluded from analysis due to ambiguity (possible missing data, true zero application, or substitution with organic manures).
  - Only records with positively applied fertiliser (rates > 0) are used; rates are treated as spatially predictable where fertiliser was applied.

## Analytical Methods
- Interpolation approach: Ordinary kriging (OK) chosen for performance, agricultural data compatibility, and ability to produce a variance surface for uncertainty estimation.
- Supporting data: Crop maps built from Land Cover plus Crops (2015–2017) using Sentinel imagery to identify crop types across two million fields.
- Processing steps:
  - Interpolate fertiliser rates per crop group using OK with a variable search radius (12 input points) to account for small sample sizes.
  - Multiply interpolated per-crop rates by crop area per 1 km cell (from Land Cover plus Crops) to obtain total application per crop.
  - Sum across crops to yield total fertiliser application per 1 km cell (kg/km2) for each fertiliser.
  - Calculations performed in ArcGIS; default OK parameters were used aside from the chosen search radius.
- Uncertainty estimation:
  - Kriging variance is computed per crop group and per fertiliser, then summed to form a single variance surface per fertiliser.
  - Uncertainty per cell is calculated as U = 2 * sqrt(V) / P * 100, giving a percentage uncertainty with ~95.5% confidence.
  - Note: summing variances assumes limited inter-crop correlation; this is a practical, conservative approach for overall uncertainty.

## Data Structure
- File format: Two-band raster TIFFs at 1 km × 1 km resolution for each fertiliser.
- File names (example):
  - fertiliser_n_prediction_uncertainty
  - fertiliser_k_prediction_uncertainty
  - fertiliser_p_prediction_uncertainty
- Band definitions:
  - Band 1: Predicted average annual fertiliser application rates (kg/km2)
  - Band 2: Uncertainty estimates associated with the predicted rates (%)

## Applications and Use Cases
- Modelling nutrient fate to predict impacts of farming practice changes (e.g., intensification/extensification) on nutrient runoff to water.
- Estimating greenhouse gas emissions linked to fertiliser use in crops and grassland, including air-quality implications.
- Quantifying historical and projected effects of eutrophication and agricultural management on ecosystems (e.g., arable plants, farmland birds, pollinators).
- Linking crop growth models to identify areas where improved nutrient management could boost yields.
- Informing policy measures to mitigate negative fertiliser impacts (e.g., catchment-sensitive farming and water quality improvements).

## Limitations and Considerations
- Zero-value records are excluded, which may omit actual non-use data or data gaps; results reflect only areas where fertilisers were applied (>0 kg/ha).
- Survey-based data are voluntary; representativeness and validation are constrained by self-selection and reporting.
- Spatial prediction relies on crop-area associations and interpolation assumptions; actual on-the-ground management may vary.
- Uncertainty is calculated under the assumption of limited cross-crop correlation when aggregating variances.

## Acknowledgements and Data Sources
- Funding: NERC national capability funding to CEH; NERC and BBSRC (NE/N018125/1) under LTS-M ASSIST.
- Data provenance: Defra’s British Survey of Fertiliser Practice (BSFP); acknowledgment of Defra’s data contributors, including David Fernall and Alison Wray.