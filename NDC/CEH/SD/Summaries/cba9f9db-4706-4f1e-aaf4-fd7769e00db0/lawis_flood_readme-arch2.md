# Gridded flood frequency estimates for Kerala, India

## Overview
- A set of six gridded datasets estimating peak river flow with return periods of 2, 5, 10, 25, 50 and 100 years across Kerala’s river network.
- Based on Central Water Commission daily river flow products; built from 23 stations spanning 2000–2020.
- Designed to provide easily accessible flood frequency estimates for engineers, policy makers and hydrology/engineering students in the region.
- Part of the LAWIS project funded by NERC/UKRI (National Capability).

## What the dataset contains
- Six ESRI ASCII grid files, each representing a single return period (2, 5, 10, 25, 50, 100 years).
- Data describe peak daily river flow magnitudes (m³ s⁻¹) on the river network in Kerala.
- Coverage is the river network (based on HydroRIVERS), gridded to align with the 15-arcsecond HydroSHEDS DEM.
- Spatial resolution: ~15 arc-seconds; extent: 74.90–77.37°E, 8.31–12.80°N; projection: WGS84.
- Grid header example (common to all files): NCOLS 593, NROWS 1076, XLLCORNER 74.8958, YLLCORNER 8.3125, CELLSIZE 0.0041667, NODATA_value -9999.
  
## How it was created (methods)
- Data source: annual maxima extracted from 23 stations (2000–2020); QC: years with <30 missing days and stations with >5 maxima retained.
- Flood frequency estimation approach:
  - QMED (median of annual maxima) modelled with a linear regression using LASSO for feature selection, based on catchment descriptors from HydroSHEDS, FAO GAEZ, and IMD rainfall grids.
  - QMED extrapolated to 318 additional sites using the catchment descriptor equation plus a spatial residual via top-kriging (rtop R package).
  - Regional growth curves for other return periods derived from a GEV distribution (Hosking-Wallis selected) fitted to annual maxima; site-specific QMED used to scale to T-year estimates (lmomRFA package).
- Quality and reproducibility:
  - Use of pre-existing CRAN packages supports reliability of outputs.
  - Techniques and data processing align with established flood frequency methodology (Flood Estimation Handbook).
  
## Data quality and validation
- Pre-quality control performed by CWC data collection.
- QC criteria applied during analysis: years with at least 30 missing days excluded; only stations with five or more annual maxima retained.
- Confidence supported by established software packages and published methods.

## Data structure and technical details
- Output format: six ESRI ASCII raster files (one per return period).
- Data values: peak daily river flow magnitudes (m³ s⁻¹).
- Area of validity: grid covers the river network of Kerala; aligned to HydroSHEDS 15-arcsecond grid.
- Supporting references and data sources include CWC India-WRIS, Flood Estimation Handbook, global hydrography datasets, and relevant statistical methods.

## Access, licensing and citation
- Data available for download under the Open Government Licence.
- Citation required when using the dataset:
  Griffin, A.; Vesuviano, G.; Cole, S. (2022). Gridded flood frequency estimates for Kerala, India. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/cba9f9db-4706-4f1e-aaf4-fd7769e00db0
- Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
- Funded by LAWIS/NERCUKRI National Capability.

## Usage and relevance for environmental monitoring
- Provides standardized, repeatable flood frequency estimates suitable for monitoring flood risk and informing policy decisions.
- Focus on accessibility and interoperability: data formatted in widely used ESRI ASCII rasters and integrated with established global datasets.
- Encourages data reuse and combination with other environmental datasets to enhance the value of flood-related monitoring and analysis.
- Suitable for engineers, policymakers, hydrology students, and researchers requiring regionally specific flood return period estimates.

## References
- Central Water Commission (2020) India-WRIS. http://india-wris.nrsc.gov.in/wrpinfo
- Robson, A., & Reed, D. (1999). Statistical procedures for flood frequency estimation (Flood Estimation Handbook, Vol. 3). Institute of Hydrology.
- Lehner, B., Verdin, K., & Jarvis, A. (2008). Global hydrography dataset (HydroSHEDS).
- Fischer, G. et al. (2008). Global Agro-ecological Zones (GAEZ 2008).
- Skøien, J. O. et al. (2006). Top-kriging on stream networks.
- Hosking, J. R. M., & Wallis, J. R. (1997). Regional Frequency Analysis (L-moments).
- Lehner, B., & Grill, G. (2013). Global river hydrography and network routing.