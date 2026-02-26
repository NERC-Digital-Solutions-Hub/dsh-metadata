# Overview of data

- A set of 24 gridded rainfall depth datasets (ESRI ARC/INFO ASCII GRID) covering Kerala, India at 0.12-degree resolution, with estimates for durations of 1, 6, 24, and 192 hours and return periods of 2, 5, 10, 25, 50, and 100 years. Each grid contains 224 point estimates across Kerala.
- Derived from the IMDAA 1-Hourly Single Level Total Precipitation dataset (1979–2020) to enable rainfall-depth estimation for ungauged sites, suitable for rainfall–runoff modelling and event rarity analyses.
- Aims to support environmental health monitoring by providing transparent, location-specific depth–duration–frequency estimates for policy and decision-making.

## Data sources and processing

- Primary data source: Indian Monsoon Data Assimilation and Analysis (IMDAA) 1-hourly rainfall dataset, hosted on the National Centre for Medium Range Weather Forecasting data portal.
- Processing steps:
  - Extract annual maximum totals for 1-, 6-, 24-, and 192-hour durations for each location across 1979–2020 (42 years).
  - For multi-hour durations, adjust year boundaries to allow accumulations to span years.
  - Compute mean annual rainfall (AAR) and the median annual maximum (RMED) plus L-moments t2 and t3.
  - Fit linear regressions to estimate RMED_e, t2,e, and t3,e as functions of latitude, longitude, duration, and AAR.
  - Fit a generalized logistic (GLO) distribution to obtain T-year rainfall depth RT_e using growth factors G_T,e.
  - Provide 2-, 5-, 10-, 25-, 50-, and 100-year depths for each duration and grid point.
- Assumptions and caveats:
  - Precipitation is treated as rainfall due to tropical climate considerations.
  - Large growth factors can occur (up to ~14 for 100-year events) in highly skewed sites; long-return-period estimates may be lower than other methods in some locations.

## Data structure and format

- Data format: ESRI ARC/INFO ASCII GRID with six header lines specifying NCOLS, NROWS, XLLCORNER, YLLCORNER, CELLSIZE, and NODATA_value.
- Grid specifics:
  - NCOLS 21, NROWS 37
  - XLLCORNER 74.82, YLLCORNER 8.34
  - CELLSIZE 0.12
  - NODATA_value -1
- Data values are in millimetres; cells outside Kerala are marked as -1 (NODATA).
- Southwesternmost data point corresponds to coordinates 74.88°E, 8.40°N.

## Methodology for rainfall-depth estimation

- Derived values include RMED, t2,e, t3,e, and e-based RMED and moments used in regression.
- Growth factors G_T,e used to scale RMED_e to T-year depths for each grid point and duration.
- Resulting RT_e values provide 2-, 5-, 10-, 25-, 50-, and 100-year rainfall depths for each duration (1, 6, 24, 192 hours).
- Global context: methodology aligns with regional frequency analysis and FEH-style approaches, with references to established literature.

## Data usage for monitoring frameworks

- Enables estimation of location-specific, duration-specific, and return-period-specific rainfall depths at ungauged sites for hydrological modelling and risk assessment.
- Supports event-based monitoring, infrastructure resilience planning, and scenario testing under varied precipitation return periods.
- Transparent provenance and metadata (including data origin, processing steps, and governing references) facilitate governance and data-sharing considerations.

## Data access, governance, and limitations

- Data governance: dataset produced under the LAWIS programme (UKRI/NERC) by UKCEH; data provenance and processing details documented to support reuse and auditability.
- Access considerations: rainfall–depth estimates are model-based and depend on IMDAA data quality; some locations may exhibit extreme growth factors affecting long-return-period estimates.
- Limitations to note:
  - Assumption that precipitation equals rainfall depth.
  - Potential metadata gaps in some inputs; dependent on the underlying IMDAA dataset quality and HydroSHEDS elevation data for altitude effects.
  - Some estimates for long return periods may diverge from direct at-site maxima due to skewness and the GLO fitting process.

## References

- Hosking, J.R.M., Wallis, J.R. (1997). Regional Frequency Analysis: An approach based on L-moments.
- Kjeldsen, T.R., Jones, D.A., Bayliss, A.C. (2008). Improving the FEH statistical procedures for flood frequency estimation.
- Lehner, B., Verdin, K., Jarvis, A. (2008). New global hydrography derived from spaceborne elevation data. Eos.