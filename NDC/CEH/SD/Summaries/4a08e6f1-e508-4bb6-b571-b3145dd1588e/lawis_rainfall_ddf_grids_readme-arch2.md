# Overview of data

## Aim
- Provide a standardized, multi-duration, multi-return-period rainfall dataset for Kerala, India to support rainfall-runoff modelling and event rarity analysis.
- Facilitate ungauged-site estimations and enable policy-relevant environmental analysis through consistent data formatting and processing.

## What it contains
- A set of 24 grids (ESRI ARC/INFO ASCII GRID format) with estimated rainfall depths.
- For each grid: 1-, 6-, 24-, and 192-hour durations; 2-, 5-, 10-, 25-, 50-, and 100-year return periods.
- 224 evenly spaced point estimates per grid covering Kerala at 0.12-degree resolution (lat/long).
- Derived from the IMDAA 1-Hourly Single Level Total Precipitation dataset (1979–2020), hosted on the National Centre for Medium Range Weather Forecasting data portal.
- Unit conversion: precipitation originally in kg/m² is treated as millimetres (assuming rainfall ≈ precipitation).

## Data processing and generation
- Source data: IMDAA rainfall depths for all India, 42-year series (1979–2020) at 0.12° resolution; altitude from HydroSHEDS (15-arcsecond DEM).
- For each Kerala point, extract annual maxima for each duration (1979–2020); for multi-hour durations, shift window by n/2 hours to allow cross-year accumulation.
- Compute mean annual rainfall (AAR) by dividing 42-year total by 42; use AAR, location, duration, and altitude in models.
- Convert rainfall totals to RMED (median of L-moment–based estimates) and L-moments t2 and t3.
- Fit regressions to estimate RMED_e, t2_e, t3_e as functions of latitude, longitude, duration, AAR, and ALT (R² values: 0.934 for RMED_e, 0.433 for t2_e, 0.446 for t3_e).
- Fit a generalized logistic (GLO) distribution to obtain rainfall depths RT_e for specified return periods, using calculated growth factors G_T,e and shape parameters from t2_e and t3_e.
- Apply to Kerela points to derive 2-, 5-, 10-, 25-, 50-, 100-year depths for durations 1, 6, 24, 192 hours.
- Note: at highly skewed sites with small medians, large growth factors (up to ~14 for 100-year events) can reduce long-period estimates relative to direct GLO fits.

## Data structure and format
- 24 grids provided as ESRI ARC/INFO ASCII GRID files.
- Each file has six header lines:
  - NCOLS 21
  - NROWS 37
  - XLLCORNER 74.82
  - YLLCORNER 8.34
  - CELLSIZE 0.12
  - NODATA_value -1
- Data section: 37 lines of 21 values each; rainfall depths in millimetres; -1 indicates data outside Kerala.
- Geospatial details: southwesternmost rainfall point near longitude 74.88°, latitude 8.40°; grid spacing 0.12°.

## Data provenance and references
- Data source: IMDAA rainfall dataset (India, 1979–2020), via ncmrwf.gov.in/data.
- Related methods and validation:
  - Regional frequency analysis using L-moments (Hosking & Wallis, 1997).
  - FEH-related statistical procedures (Kjeldsen et al., 2008).
  - Global hydrography integration (Lehner et al., 2008).
- Funder: UKRI (NERC) UKCEH National Capability LAWIS programme.
- Authors: Gianni Vesuviano, Adam Griffin, Lisa Stewart, Steve Cole (UKCEH).