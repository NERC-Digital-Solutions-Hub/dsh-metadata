# A set of 24 grids (ESRI ARC/INFO ASCII GRID format), each containing estimated rainfall depths for a rainfall event of duration 1, 6, 24 or 192 hours and return period 2, 5, 10, 25, 50 or 100 years.

## Overview
- A collection of 24 grids, each in ESRI ARC/INFO ASCII GRID format, covering Kerala, India at 0.12-degree resolution with 224 point estimates per grid.
- Values represent estimated rainfall depths (mm) for rainfall-event durations of 1, 6, 24, and 192 hours and return periods of 2, 5, 10, 25, 50, and 100 years.
- Generated to enable estimation of rainfall depths at ungauged sites for applications such as rainfall–runoff modelling and event rarity analysis.
- Based on the IMDAA 1-Hourly Single Level Total Precipitation dataset (1979–2020), sourced from the Indian National Centre for Medium Range Weather Forecasting (NCMRWF).

## Source data and lineage
- IMDAA rainfall dataset: hourly rainfall depths for all India, 1979–2020, at 0.12° resolution; units kg/m^2 (treated as mm).
- Data processing focused on annual maxima for durations 1, 6, 24, and 192 hours for each year, with careful handling of year boundaries to allow multi-year accumulations.
- Derived metrics per location: RMED (median of annual maxima), t2 and t3 (L-moment ratios).
- Altitude data from HydroSHEDS (15-arcsecond DEM) used as a predictor.
- All transformations and calculations are explicitly documented, including unit conversions (kg/m^2 to mm) and the interpretation of rainfall as precipitation due to Kerala’s tropical climate.

## Processing workflow and modeling
- For each point in Kerala, computed 42 annual maxima per duration (1979–2020) and derived:
  - RMED_e: median of RMED estimates
  - t2_e and t3_e: L-moment ratios
- Linear regression models fitted to RMED_e, t2_e, and t3_e with predictors: Latitude, Longitude, Duration, AAR (mean annual rainfall), ALT (altitude).
  - Models show strong explanatory power for RMED_e (adjusted R² ≈ 0.934), with moderate explanatory power for t2_e and t3_e (adjusted R² ≈ 0.433 and 0.446).
- Generalized logistic (GLO) distribution fitted to each set (RMED_e, t2_e, t3_e) to estimate rainfall depth RT_e for specified return periods T:
  - RT_e = RMED_e × G_T,e
  - G_T,e defined via growth factors GT,e with parameters derived from the e-set (β_e, κ_e) and the return period T
  - κ_e = −t3,e; β_e computed from t2,e, κ_e, and duration-related terms
- Application step yields rainfall depths for 2-, 5-, 10-, 25-, 50-, and 100-year periods across durations 1, 6, 24, and 192 hours.
- Important caveat: large growth factors may occur (up to ~14 for 100-year events) in locations with highly skewed annual maxima, which can lead to longer-period estimates that are lower than at-site estimates derived directly from annual maxima.

## Data structure and format
- Files: 24 ESRI ARC/INFO ASCII GRID files with identical 6-header-line metadata.
- Grid dimensions: 21 columns × 37 rows; cell size 0.12 degrees.
- Spatial reference: southwestern corner at XLLCORNER 74.82, YLLCORNER 8.34 (WGS84).
- Data values: rainfall depths in millimetres; nodata as -1 for locations outside Kerala.
- Data content: values stored as plain text; outside-domain values set to -1.

## Metadata and documentation
- Data provenance, processing steps, and modeling approach are described in detail, including:
  - Source data and processing for annual maxima
  - Statistical modeling with L-moments and generalized logistic distribution
  - Regression equations and parameter interpretation
- References cited for methodological foundations:
  - Hosking & Wallis (1997)
  - Kjeldsen, Jones, Bayliss (2008)
  - Lehner, Verdin, Jarvis (2008)
- Funded under UKRI/NERC LAWIS National Capability; authors affiliated with UKCEH.

## Usage notes and governance considerations
- Reuse implications for data stewards:
  - Clear data lineage from IMDAA rainfall through to UKCEH-generated grids, including data transformations and modeling steps.
  - Explicit unit handling (kg/m^2 ≈ mm) and geographic context (Kerala, 0.12° grid) to ensure consistent interpretation across systems.
  - Metadata should capture the dependencies on AAR and ALT predictors, the regression-based RMED/t2/t3 derivations, and the GLO-based RT_e estimation.
  - Acknowledgement of limitations for long return periods, especially in regions with skewed maxima where growth factors can be large.
  - Awareness of potential interoperability considerations when linking these grids with other formats or higher-resolution datasets.
- Potential challenges aligned with data steward experience:
  - Ensuring ongoing availability or updates if source IMDAA data are updated.
  - Maintaining consistent metadata standards across all 24 grids to support discoverability and reuse.
  - Handling format interoperability if data are ported to non-ASCII formats or different GIS environments.

## Availability and contact
- Project context: LAWIS program under UKRI/NERC.
- Data custodian: UKCEH.
- Version/date: 2022-05-19 (version 1.0).
- References and methodological notes provided for reproducibility and validation.