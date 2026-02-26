# Gridded flood frequency estimates for Kerala, India

## Overview
- A set of six gridded datasets providing estimates of peak river flow with return periods of 2, 5, 10, 25, 50 and 100 years across the Kerala river network.
- Based on Central Water Commission (CWC) daily river flow products for 2000–2020; data are available as Open Government Licence.
- Meant to support engineers, policy makers and hydrology students with accessible flood frequency information.

## Data content and structure
- Format: six ESRI ASCII grid files, each corresponding to a return period (2, 5, 10, 25, 50, 100 years).
- Grid details shown in the header:
  - NCOLS 593, NROWS 1076
  - XLLCORNER 74.8958, YLLCORNER 8.3125
  - CELLSIZE 0.0041667
  - NODATA_value -9999
- Projection and extent:
  - WGS 84
  - 15 arc-second resolution
  - Extent: 74.90 – 77.37 E, 8.31 – 12.80 N
- Data represent peak daily river flow (m^3 s^-1) across the river network, tied to HydroRIVERS network data and gridded to align with HydroSHEDS resolution.

## Data collection and generation
- Source data: 23 gauging stations in Kerala with daily river flow; time window 2000–2020.
- Quality control at collection: annual maxima reported only for years with fewer than 30 missing days; only stations with more than 5 annual maxima retained.
- Modelling approach:
  - QMED (median of annual maxima) estimated via linear regression with LASSO using catchment descriptors derived from HydroSHEDS, FAO GAEZ soil data, and IMD rainfall products.
  - QMED then used to estimate 2–100 year events at 318 sites; a spatially consistent residual added via top-kriging.
  - Regional growth curves created with the Generalized Extreme Value (GEV) distribution (Hosking-Wallis test used for selection).
  - Site-specific QMED scales to true T-year estimates using the lmomRFA package.
- Quality and reproducibility:
  - Uses pre-existing CRAN packages, supporting model reliability and reproducibility.
  - Output quality benefits from CWC data QC and validated statistical methods.

## Data governance, provenance and funding
- Project: LAWIS (Lawis) funded under National Capability by UKRI; builds on SUNRISE activities in Maharashtra, India.
- Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
- Data provenance links to Central Water Commission (India) data and multiple supporting datasets (HydroSHEDS, GAEZ, FAO, IMD).

## Licensing, citation and access
- Access: Open Government Licence; dataset available via DOI.
- Citation requirement: Griffin, A.; Vesuviano, G.; Cole, S. (2022). Gridded flood frequency estimates for Kerala, India. NERC Environmental Information Data Centre (Dataset). DOI: 10.5285/cba9f9db-4706-4f1e-aaf4-fd7769e00db0
- Usage terms: By downloading, accessing or using the dataset, users agree to the licence terms and must cite the dataset accordingly.

## User considerations and practical guidance
- Target users: engineers, policy makers, hydrology/engineering students; intended to be accessible for planning and educational purposes.
- How to use: provide location-specific flood frequency estimates across the Kerala river network for planning, design, and risk assessment.
- Limitations and caveats:
  - Data limited to 23 gauged stations and 2000–2020 period; interpolation and regional growth methods introduce uncertainty, especially in less-well-sampled areas.
  - The dataset covers the river network only; does not include non-network hydrological features outside the HydroRIVERS-defined network.
  - Future updates would require new data sources and reprocessing to maintain currency.

## Metadata and discoverability
- Clear linkage to data lineage, methods, and supporting references.
- Documentation includes specifics on file structure, projection, and grid resolution to aid discoverability and reuse.
- Encourages collaboration and broader community use to support an effective data system for flood risk assessment.