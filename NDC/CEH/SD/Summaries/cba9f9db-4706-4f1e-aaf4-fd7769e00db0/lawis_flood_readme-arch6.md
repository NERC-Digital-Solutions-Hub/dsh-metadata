# Gridded flood frequency estimates for Kerala, India

## Overview
- A set of six gridded datasets (ESRI ASCII) showing peak river flow estimates for return periods 2, 5, 10, 25, 50 and 100 years across Kerala’s river network.
- Based on Central Water Commission daily river flow products (2000–2020) from 23 stations; QA ensures years with <30 missing days and stations with >5 annual maxima are included.
- Methodology follows flood frequency practices: QMED modeled via LASSO regression using catchment descriptors from HydroSHEDS, GAEZ, FAO soil data, and IMD rainfall grids; a spatially consistent residual added via top-kriging (rtop R package).
- Extension to other return periods uses a regional growth curve from the GEV distribution (Hosking-Wallis test) and site-specific QMED scaling (lmomRFA).
- Outputs rely on pre-existing CRAN packages to support quality and reproducibility.
- Data are mapped to the river network (HydroRIVERS) and converted to a grid aligned with the 15-arcsecond HydroSHEDS DEM.

## Data access and licensing
- Open Government Licence; download URL provided with the dataset.
- Data usage requires agreeing to licence terms and citing the dataset: Griffin, A.; Vesuviano, G.; Cole, S. (2022). Gridded flood frequency estimates for Kerala, India. NERC Environmental Information Data Centre.
- Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
- Funded by the LAWIS project under NERC/UKRI National Capability.

## Data collection and generation
- Six files (one per return period) derived from 23 station annual maxima (2000–2020).
- QA criteria applied at the data source and analysis stages to ensure data robustness.
- Method integrates catchment descriptors and regional growth curves to produce nationwide gridded estimates for Kerala.

## Data structure
- Each file contains peak daily river flow magnitudes (m³/s) for return periods 2, 5, 10, 25, 50, and 100 years.
- ESRI ASCII format with consistent header details:
  - NCOLS 593, NROWS 1076
  - XLLCORNER 74.8958, YLLCORNER 8.3125
  - CELLSIZE 0.0041667
  - NODATA_value -9999
- Projection: WGS 84; resolution: 15 arc-seconds; extent: 74.90–77.37°E, 8.31–12.80°N.

## Quality control
- Pre-processing quality checks by CWC; years with excessive missing data excluded; stations with insufficient annual maxima excluded.
- Use of established CRAN packages supports reliable, reproducible code and results.

## Practical use for data support
- Ready-to-use data products for engineers, policymakers, and hydrology students to assess flood risks in Kerala.
- Suitable for GIS analysis, dashboarding, or integration with other hydrological or risk datasets to support decision-making.
- Clear licensing and citation requirements facilitate responsible data sharing and provenance tracking.
- Potential to extend methodology to other regions or update with new station data, while maintaining a consistent GRP-based framework.

## References
- Central Water Commission (India-WRIS) data sources.
- Robson & Reed (Flood Estimation Handbook) procedures.
- Lehner et al. (Global hydrography) and related data sources used for descriptors.
- Skøien et al. (Top-kriging on stream networks) and Hosking & Wallis (Regional frequency analysis) methodologies.
- Lehner & Grill (Global river hydrography) supporting network data basis.