# A set of 24 grids (ESRI ARC/INFO ASCII GRID format), each containing estimated rainfall depths for a rainfall event of duration 1, 6, 24 or 192 hours and return period 2, 5, 10, 25, 50 or 100 years.

## Purpose and scope
- Provides rainfall depth estimates for ungauged sites in Kerala, India, to support rainfall-runoff modelling and event rarity analysis.
- Part of the LAWIS project funded by UKRI (NERC) under UKCEH National Capability.

## Data contents
- 24 gridded datasets, each in ESRI ARC/INFO ASCII GRID format.
- Resolution: 0.12 degrees.
- Coverage: state of Kerala, with 224 valid data points; values outside Kerala encoded as -1 (NODATA).

## Data source
- Derived from the Indian Monsoon Data Assimilation and Analysis (IMDAA) 1-Hourly Single Level Total Precipitation dataset (1979–2020).
- IMDAA provides hourly rainfall depths for all of India at 0.12° resolution; unit is kg/m2 (treated as mm for rainfall depth).

## Processing and generation
- For each valid point in Kerala, annual maxima were extracted for durations of 1, 6, 24, and 192 hours across 42 years (1979–2020).
- For multi-hour durations, year boundaries were adjusted by appending hours at start/end to span two years if needed.
- The mean annual rainfall (AAR) was computed as the 42-year mean.
- For each point and duration, the median (RMED) and first two L-moment ratios (t2, t3) were calculated.
- Linear regressions were fitted to estimate e-values (RMED_e, t2_e, t3_e) as functions of latitude, longitude, duration, and AAR (altitude used later).

## Altitude data
- Altitude at each location derived from HydroSHEDS 15-arcsecond digital elevation model.

## Estimation of rainfall depths for specified return periods
- A generalized logistic (GLO) distribution was fitted to RMED_e, t2_e, and t3_e.
- Estimated rainfall depth RT_e for a T-year return period:
  - RT_e = RMED_e * G_T,e
  - G_T,e = 1 + (beta_e / kappa_e) * [1 - (T - 1)^(-kappa_e)]
  - kappa_e = -t3_e
  - beta_e = [t2_e * kappa_e * sin(pi * kappa_e)] / [kappa_e * pi * (kappa_e + t2_e) - t2_e * sin(pi * kappa_e)]
- Applied to compute 2-, 5-, 10-, 25-, 50-, and 100-year depths for durations of 1, 6, 24, and 192 hours.
- Note: in locations with highly skewed annual maxima, large growth factors can occur (up to ~14 for a 100-year event); at long return periods, estimates can be less than those from direct at-site fitting.

## Data structure and format
- Each grid includes six header lines with:
  - NCOLS 21
  - NROWS 37
  - XLLCORNER 74.82
  - YLLCORNER 8.34
  - CELLSIZE 0.12
  - NODATA_value -1
- Data values follow in 37 lines of 21 values each; values are in millimetres.
- Values outside Kerala are -1 (NODATA).

## Practical uses for GIS
- Map-based retrieval of rainfall depths for specific durations and return periods at ungauged sites.
- Integration with hydrological, flood frequency, or climate-impact analyses within GIS workflows.
- Ability to combine with other spatial datasets (e.g., land use, soils, DEM) for ensemble modelling or risk assessment.

## Limitations and caveats
- Data are point estimates derived from gridded IMDAA inputs; uncertainties arise from interpolation, model assumptions, and regional fitting.
- Long-return-period estimates may be conservative or lower than direct at-site estimates in skewed locations due to growth-factor behavior.

## References
- Hosking, J.R.M., Wallis, J.R. (1997). Regional Frequency Analysis: An approach based on L-moments.
- Kjeldsen, T.R., Jones, D.A., Bayliss, A.C. (2008). Improving the FEH statistical procedures for flood frequency estimation.
- Lehner, B., Verdin, K., Jarvis, A. (2008). New global hydrography derived from spaceborne elevation data.

## Credits
- Authors: Gianni Vesuviano, Adam Griffin, Lisa Stewart, Steve Cole - UKCEH
- Funders: UKRI (NERC); UKCEH National Capability: LAWIS programme
- Date of upload: 2022-05-19 (version 1.0)