# Gridded flood frequency estimates for Kerala, India

## Overview
- Dataset providing estimates of peak river flow with six return periods (2, 5, 10, 25, 50, 100 years) across Kerala, India.
- Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
- Funded by LAWIS project, NERC/UKRI National Capability.
- Access and licensing: Open Government Licence; dataset downloadable from the provided DOI; must cite Griffin, Vesuviano, and Cole (2022).
- Intended audience: engineers, policy makers, hydrology/engineering students; designed to be easily accessible for monitoring and decision-making.

## Data content and structure
- Six gridded ESRI ASCII files, one per return period (2, 5, 10, 25, 50, 100 years).
- Grid specification:
  - NCOLS 593, NROWS 1076
  - XLLCORNER 74.8958, YLLCORNER 8.3125
  - CELLSIZE 0.0041667 degrees (15 arc-second resolution)
  - Extent: 74.90–77.37 E, 8.31–12.80 N
  - Projection: WGS 84
  - NODATA_value: -9999
- Coverage: based on the river network, aligned to HydroRIVERS; data gridded to the HydroSHEDS 15-arcsecond terrain model resolution.
- Content: peak daily river flow magnitudes (m3 s-1) for each return period.

## Data collection and generation
- Source data: annual maxima extracted from Central Water Commission (CWC) daily river flow products for 23 stations in Kerala (2000–2020).
- Quality control at collection: only years with fewer than 30 missing days; only stations with more than 5 annual maxima retained.
- Methodology:
  - Flood frequency estimation follows procedures similar to the Flood Estimation Handbook.
  - QMED (median of the annual maxima) modeled via linear regression with LASSO to relate to catchment descriptors.
  - Catchment descriptors derived from HydroSHEDS, FAO GAez, and IMD rainfall products.
  - QMED estimated at 318 additional sites using the descriptor equation; spatially consistent residual added via top-kriging (rtop R package).
  - Regional growth curves for higher return periods derived using GEV distribution (Hosking-Wallis test) and scaled to true T-year events using site-specific QMED (lmomRFA).
- Data provenance and quality tools:
  - Use of pre-existing CRAN packages to support modeling and quality assurance.
  - Data structure rooted in established river network datasets (HydroRIVERS, HydroSHEDS).

## Data governance and access
- Data is publicly shareable under the Open Government Licence; users must cite the original authors.
- Data exists on the river network domain; gridded outputs reflect network-based coverage rather than a full-area raster.
- Clear metadata references and links to the contributing data sources (CWC, HydroSHEDS, GAEZ, FAO, IMD) to support traceability.

## Quality control and reliability
- QC steps taken at data collection and analysis stages:
  - CWC pre-checks for data completeness.
  - Station-level filtering based on missing data and number of maxima.
  - Reliability supported by documented methodology (FEH-like procedures, LASSO regression, top-kriging, GEV-based extrapolation).
- Confidence implied by use of established CRAN packages for computation and validation.

## Applications and intended use
- Designed for engineers, policymakers, and students to support flood risk assessment, infrastructure planning, and policy monitoring.
- Enables comparison of observed and modeled flood frequencies across Kerala, with standardized return periods and spatially consistent estimates.

## References
- Data sources and methodologies cited, including India-WRIS (CWC), Flood Estimation Handbook, HydroSHEDS, GAEZ, FAO, IMD rainfall products, top-kriging framework, Hosking-Wallis regional frequency analysis, and related hydrological data frameworks.