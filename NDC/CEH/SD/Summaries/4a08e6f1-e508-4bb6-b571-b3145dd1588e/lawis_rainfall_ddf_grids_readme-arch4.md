# Overview of data

- What the dataset is: A set of 24 gridded rainfall depth estimates for Kerala, India, covering durations of 1, 6, 24, and 192 hours and return periods of 2, 5, 10, 25, 50, and 100 years. Each grid provides rainfall depths at 0.12-degree resolution for 224 valid points within Kerala (values outside Kerala are marked as nodata).
- Purpose: Enables estimation of rainfall depths for arbitrary duration and return period at ungauged sites, supporting rainfall–runoff modelling and event rarity analysis.

## Data provenance and sources

- Primary input: IMDAA (Indian Monsoon Data Assimilation and Analysis) 1-hourly total precipitation dataset (1979–2020), hourly rainfall depths across India at 0.12° resolution.
- Data host: IMDAA data portal hosted by the National Centre for Medium Range Weather Forecasting (ncmrwf.gov.in/data).
- Derived data: 42 annual maxima per location and duration, mean annual rainfall (AAR), and summary statistics (RMED, t2, t3) used to fit generalized models.
- Ancillary data: Altitude from HydroSHEDS 15-arcsecond digital elevation model.

## Processing methodology

- Annual maxima extraction: For each location and duration, 42 yearly maxima (1979–2020) are computed, with special handling to allow multi-year accumulation when maxima span year boundaries.
- Summary statistics: Compute RMED (median of annual maxima) and L-moment ratios t2 and t3.
- Regression framework: Fit linear regressions to RMED, t2, and t3 using latitude, longitude, duration, and AAR (and altitude in the broader formulation).
- Growth and distribution: Use a generalized logistic (GLO) distribution fitted to RMED and L-moments to estimate return-period rainfall depths for the specified durations and locations.
- Return-period estimation: Compute T-year rainfall depth RT_e as RMED_e multiplied by a growth factor G_T,e, with G_T,e defined by parameters derived from t2,e and t3,e.
- caveat: In locations with highly skewed annual maxima and low medians, the model can yield very large growth factors (up to ~14 for 100-year events); in some cases, longer-return-period estimates may be lower than those obtained by direct at-site extrapolation.

## Data structure and format

- File format: 24 ESRI ARC/INFO ASCII GRID files.
- Grid metadata (same across all files): 
  - NCOLS 21, NROWS 37
  - XLLCORNER 74.82, YLLCORNER 8.34
  - CELLSIZE 0.12
  - NODATA_value -1
- Data layout: 37 lines of data with 21 values per line; values are in millimetres (mm). Values of -1 indicate locations outside Kerala.
- Spatial coverage: The southwestern corner corresponds to a specific latitude/longitude; the grid spacing is uniform, but only 224 interior points carry valid estimates within Kerala (others are nodata).

## Key variables and definitions

- Durations covered: 1, 6, 24, 192 hours
- Return periods: 2, 5, 10, 25, 50, 100 years
- RMED_e: median of the 42-year annual maxima series for location e
- t2,e and t3,e: L-moment ratios for location e
- RMEDe: estimated RMED at location e
- GT,e: growth factor for a given return period
- RT_e: rainfall depth for return period T at location e
- AAR: average annual rainfall at location e
- ALT: altitude at location e (from HydroSHEDS)

## Applications and use cases

- Estimating rainfall depths for ungauged sites across specified durations and return periods.
- Supporting rainfall–runoff modelling, hazard assessment, and event rarity analysis in Kerala and similar tropical contexts.

## Data access, governance, and limitations

- Access: Data delivered as ASCII GRID files; hosted resources referenced (IMDAA data and HydroSHEDS for altitude).
- Metadata and discoverability: Clear header metadata and explicit nodata handling aid in discoverability and reuse.
- Limitations and cautions: Heavy-tailed growth factors can yield extreme estimates for long return periods in skewed locations; users should interpret high return-period depths with caution and consider local context and alternative methods for verification.

## References

- Hosking, J.R.M., Wallis, J.R. (1997). Regional Frequency Analysis: An approach based on L-moments.
- Kjeldsen, T.R., Jones, D.A., Bayliss, A.C. (2008). Improving the FEH statistical procedures for flood frequency estimation.
- Lehner, B., Verdin, K., Jarvis, A. (2008). New global hydrography derived from spaceborne elevation data.