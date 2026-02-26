# Overview of data

## Data Scope and Purpose
- A set of 24 grids (ESRI ARC/INFO ASCII GRID format) containing estimated rainfall depths for rainfall events with durations of 1, 6, 24, and 192 hours.
- Return periods covered: 2, 5, 10, 25, 50, and 100 years.
- Grids cover the state of Kerala, India, at 0.12-degree resolution; each grid is a 21x37 cell array (data in mm, with -1 as NODATA outside Kerala).
- Purpose: enable estimation of rainfall depths for arbitrary duration and return period at ungauged sites (useful for rainfall–runoff modelling and event rarity analyses).
- Source data: IMDAA 1-Hourly Single Level Total Precipitation for all of India (1979–2020), hosted on the National Centre for Medium Range Weather Forecasting portal. The processing converts hourly data to annual maxima and site-specific estimates.

## Data Contents
- 24 grids, each containing rainfall depth estimates (mm) for the four durations across the six return periods.
- Spatial extent defined by a 0.12° grid; the southwestern corner coordinates are provided in each grid’s header.
- Data values outside Kerala are marked as -1 (NODATA).

## Processing and Generation (Data Pipeline)
- Source: IMDAA hourly rainfall data (1979–2020, 42 years, excluding the first six hours of 1979).
- For each grid point and duration:
  - Extract 42 annual maxima for each duration.
  - To enable multi-hour accumulations spanning year boundaries, adjust year alignment by shifting half the duration (n/2 hours) at the start/end of years as needed.
  - Compute mean annual rainfall (AAR) by dividing the 42-year total by 42.
  - Treat precipitation as rainfall and convert kg/m^2 to mm.
  - Compute RMED (median of the 42 annual maxima) and L-moments t2 and t3.
  - Fit linear regressions to obtain location-specific estimates (RMEDe, t2,e, t3,e) as functions of latitude, longitude, duration, and ln(AAR); altitude (ALT) from HydroSHEDS is included in the variables.
  - Report adjusted R^2 values for RMEDe (0.934), t2,e (0.433), and t3,e (0.446).

## Estimation Methodology (Return-Period Rainfall Depths)
- For each point, fit a generalized logistic (GLO) distribution to RMEDe, t2,e, and t3,e.
- Estimate rainfall depth Re for a specified return period T (years) as Re = RMEDe × G_T,e, where G_T,e is the T-year growth factor:
  - G_e = 1 + (beta_e / kappa_e) × [1 − (T − 1)^(−kappa_e)]
  - kappa_e = −t3,e
  - beta_e = [t2,e × kappa_e × sin(π × kappa_e)] / [kappa_e × π × (kappa_e + t2,e) − t2,e × sin(π × kappa_e)]
- Application: derives 2-, 5-, 10-, 25-, 50-, and 100-year rainfall depths for each duration (1, 6, 24, 192 hours) at every grid point.
- Caveat: in locations with highly skewed maxima and low medians, growth factors can be large (up to ~14 for a 100-year event). In such cases, longer-return-period estimates may be lower than those produced by a direct GLO fit to at-site maxima.

## Data Structure and Access
- Each grid file uses ESRI ASCII GRID format with a uniform header:
  - NCOLS 21, NROWS 37
  - XLLCORNER 74.82, YLLCORNER 8.34
  - CELLSIZE 0.12
  - NODATA_value -1
- Data values are plain mm; outside-kerala values are -1.
- Southwest corner and grid cell spacing define the geographic positioning; data are organized as 37 rows of 21 values each.
- Data originate from IMDAA rainfall data portal (ncmrwf.gov.in) and are produced under the UKRI LAWIS programme (National Capability).

## Usage Considerations
- The approach combines empirical site–factors (latitude, longitude, altitude) with duration and regional rainfall context (AAR) to estimate at ungauged sites.
- The modeling relies on linear regressions for RMEDe, t2,e, t3,e and a GLO distribution for return-period depths; accuracy depends on data quality of IMDAA and the representativeness of Kerala’s maxima.
- Users should be aware of potential extrapolation when applying to locations with limited local rainfall variability or unusual topography.

## References
- Hosking, J.R.M., & Wallis, J.R. (1997). Regional Frequency Analysis: An approach based on L-moments. Cambridge University Press.
- Kjeldsen, T.R., Jones, D.A., Bayliss, A.C. (2008). Improving the FEH statistical procedures for flood frequency estimation. Environment Agency.
- Lehner, B., Verdin, K., Jarvis, A. (2008). New global hydrography derived from spaceborne elevation data. Eos, Transactions, American Geophysical Union.