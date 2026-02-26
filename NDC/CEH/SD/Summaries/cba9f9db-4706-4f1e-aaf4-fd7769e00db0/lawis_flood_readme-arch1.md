# Data access and citation

- Overview
  - Six gridded datasets (ESRI ASCII) estimating peak river flow with return periods of 2, 5, 10, 25, 50 and 100 years across Kerala, India.
  - Based on annual maxima from 23 CWC stations (2000–2020); QC: include years with fewer than 30 missing days and retain stations with more than 5 annual maxima.
  - Methodology mirrors Flood Estimation Handbook approaches: QMED via linear regression with LASSO using catchment descriptors; regional growth curves via GEV distribution for other return periods; site-specific scaling using QMED and top-kriging residuals.

- Data access, license, and citation
  - Open Government Licence; data downloadable at doi: 10.5285/cba9f9db-4706-4f1e-aaf4-fd7769e00db0.
  - Must cite: Griffin, A.; Vesuviano, G.; Cole, S. (2022). Gridded flood frequency estimates for Kerala, India. NERC Environmental Information Data Centre (Dataset).

- Authors and funding
  - Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
  - Funded by the LAWIS project, NERC/UKRI National Capability.

- Data collection and generation details
  - Data scope: peak daily river flow magnitudes (m3 s-1) for six return periods across Kerala’s river network.
  - Source data: Central Water Commission daily river flow products; 2000–2020 maxima.
  - Quality control: exclude years with ≥30 missing days; retain stations with >5 maxima.
  - Descriptor sources: HydroSHEDS, UN FAO Harmonised World Soil Database, IMD rainfall gridded products.
  - QMED estimation: regression (LASSO) based on catchment descriptors; QMED extended to 318 sites; residual corrected with top-kriging (rtop R package).
  - T-year events: regional growth curves via GEV distribution (Hosking-Wallis); site-specific QMED scaling; lmomRFA package used.
  - Data provenance: relies on pre-existing CRAN packages for quality assurance.

- Data structure and format
  - Six ESRI ASCII files, each representing a return period (2, 5, 10, 25, 50, 100 years).
  - Header/example: NCOLS 593, NROWS 1076, XLLCORNER 74.8958, YLLCORNER 8.3125, CELLSIZE 0.0041667, NODATA_value -9999.
  - Projection/extent: WGS 84, 15-arc-second resolution; extent 74.90–77.37°E, 8.31–12.80°N.
  - Spatial basis: data anchored to HydroRIVERS river network, converted to a grid matching the HydroSHEDS resolution.

- Practical usage and aims
  - Intended to provide readily accessible flood frequency estimates and methods for engineers, policymakers, and hydrology/engineering students.
  - Builds a reproducible workflow with clear data sources and statistical approaches to support decision-making in flood risk assessment.

- Data provenance and references
  - Key sources include India-WRIS (CWC), Flood Estimation Handbook, HydroSHEDS, GAEZ, top-kriging methodology, Hosking-Wallis regional frequency analysis, and global river hydrography work (Lehner & Grill).