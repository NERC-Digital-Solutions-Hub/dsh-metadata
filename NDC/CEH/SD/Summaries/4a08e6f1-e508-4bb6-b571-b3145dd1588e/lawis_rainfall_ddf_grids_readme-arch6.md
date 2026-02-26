# Overview of data

- What the dataset is
  - A set of 24 grids (ESRI ARC/INFO ASCII GRID format) containing estimated rainfall depths for rainfall event durations of 1, 6, 24, or 192 hours and return periods of 2, 5, 10, 25, 50, or 100 years.
  - Grids cover Kerala, India at 0.12-degree resolution; each grid contains 224 point estimates within Kerala (values outside Kerala are -1).
  - Units are millimetres (converted from the original kg/m^2, assumed equivalent to rainfall depth). Precipitation is treated as rainfall due to Kerala’s tropical climate.
  - Derived from the IMDAA 1-Hourly Single Level Total Precipitation dataset (1979–2020, 42 years), enabling estimation of rainfall depths for arbitrary duration/return period at ungauged sites for rainfall–runoff modelling and event rarity analysis.

- Data processing and generation
  - Use IMDAA hourly rainfall data (1979–2020) to obtain annual maximum totals for 1-, 6-, 24-, and 192-hour durations for each year and grid point.
  - For multi-hour totals (n > 1), shift year boundaries by n/2 hours to allow maxima spanning year boundaries.
  - Compute mean annual rainfall (AAR) as the 42-year average for each location.
  - Derive RMED_e (median of annual maxima) and L-moment ratios t2_e, t3_e from the 42-year series.
  - Fit linear regressions to estimate RMED_e, t2_e, t3_e as functions of latitude, longitude, duration, and AAR.
  - Fit a generalized logistic (GLO) distribution to each set of RMED_e, t2_e, t3_e and estimate rainfall depth RT_e for specified return periods T.
  - Calculate growth factor G_T,e with parameters derived from t2_e and t3_e; compute RT_e = RMED_e × G_T,e.
  - Note: in highly skewed locations, large growth factors (up to ~14 for 100-year events) may yield longer-period estimates that are lower than a direct GLO fit to site maxima.

- Data structure and access
  - Each of the 24 grids is provided in ESRI ARC/INFO ASCII GRID format.
  - Header example: NCOLS 21, NROWS 37, XLLCORNER 74.82, YLLCORNER 8.34, CELLSIZE 0.12, NODATA_value -1.
  - Data region corresponds to Kerala; data values are rainfall depths in millimetres; cells outside Kerala are -1 (NODATA).

- Provenance and references
  - Authors: Gianni Vesuviano, Adam Griffin, Lisa Stewart, Steve Cole (UKCEH)
  - Funders: UKRI (NERC) LAWIS programme, LAWIS National Capability
  - Source dataset: IMDAA 1-Hourly Single Level Total Precipitation (ncmrwf.gov.in/data), India (1979–2020)
  - Key references: Hosking & Wallis (L-moments), Kjeldsen et al. (GLO distribution), Lehner et al. (HydroSHEDS elevation)

- Practical use and caveats
  - Intended for estimating rainfall depths at specified durations and return periods at ungauged locations within Kerala; supports rainfall–runoff modelling and event rarity analyses.
  - Caveats include potential extreme-growth-factor behavior at skewed sites; be mindful of possible discrepancies between long-return-period estimates and direct at-site fits in highly skewed regions.
  - Data integration and quality considerations: derived from a single large dataset (IMDAA) with regression-based upscaling to RTe estimates; units and transformations are explicitly documented.

- Metadata snapshot
  - Date of upload: 2022-05-19 (version 1.0)
  - Context: part of the LAWIS project under UKRI/NERC National Capability
  - Use-case alignment: supports estimation of rainfall depths at ungauged sites for hydrological analyses and risk assessment in Kerala, India