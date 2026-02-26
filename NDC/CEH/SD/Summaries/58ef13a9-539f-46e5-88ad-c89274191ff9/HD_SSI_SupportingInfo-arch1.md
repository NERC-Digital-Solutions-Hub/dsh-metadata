# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

## Overview
- Dataset provides Standardised Streamflow Index (SSI) values for 303 UK catchments.
- SSI is a drought index based on the cumulative probability of monthly mean streamflow for a catchment.
- Calculated for accumulation periods of 1, 3, 6, 9, 12, 18 and 24 months, assigned to the end of each accumulation period.
- Data span: 1891–2015; standard Tweedie distribution period used for fitting: 1961–2010.
- Stored as CSV files; each file corresponds to a catchment/flow series and includes all seven accumulation periods.
- Project context: part of Historic Droughts (2014–2018) funded by UK Research Councils; involved eight institutions.

## What SSI measures and how it’s calculated
- SSI uses the cumulative probability of observed monthly streamflow for a catchment, transformed to a Normal distribution with mean 0 and SD 1 (normal scores), producing unitless values.
- Negative SSI values indicate drier-than-average conditions; positive values indicate wetter-than-average conditions.
- Range is truncated to -5 to +5 due to uncertainty at distribution extremes.

## Data & Methods in brief
- Source data: Historic Reconstructions of Daily River Flow for 303 UK catchments (1891–2015); includes modelled daily flows, calibrated to naturalised flow series for some catchments (305 series total when including calibrations).
- Catchment selection includes near-natural and artificial-influenced sites; calibration quality shown with NSE metrics (1982–2014) and other evaluation metrics (available per catchment).
- SSI computation:
  - Fit Tweedie distribution to monthly/accumulated streamflows for each accumulation period.
  - Transform to normal scores (mean 0, SD 1); end-month assignment for each accumulation period.
  - Note: overlapping data for accumulation periods >12 months can introduce autocorrelation; independence assumptions for frequency analysis are violated in such cases.
- Software/tools:
  - Tweedie distribution via R packages tweedie and SCI, with custom scripts to enable calculations.
- Standard period alignment:
  - 1961–2010 used to align with SPI calculations within the Historic Droughts project.

## Data format and structure
- File naming: "HD_SSI_<CatchId>_189101-201511.csv" (one file per catchment/flow series).
- Contents:
  - SSI values for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months (end-month of each accumulation).
  - Data are normal scores with no units; values restricted to -5 to 5.
- Missing data:
  - Indicated by -999.
  - Start months and counts of initial missing values differ by accumulation period (Table 1 in the dataset notes).
  - Some catchments have long periods with missing data where the Tweedie distribution could not be fitted for monthly data (e.g., catchments 31023 and 39017).
  - Additional months with missing SSI values exist (Table 3) due to fitting issues; total missing across all series: 64 values affecting 42 catchments (Table A1).
- Supplementary catchment information:
  - HD_SSI_CatchInfo.csv lists catchment details:
    - Catchid, NRFACatchmentName, Area_sqkm, Nested flag, UKBN2_LFBN flag, NRFA_StationPage URL.

## Data quality and caveats
- SSI values are based on modelled reconstructions of daily river flow; data quality varies by catchment and period.
- Calibration and evaluation details are documented (e.g., NSE) and available with the data.
- For accumulation periods longer than 12 months, data overlap can introduce autocorrelation; interpretation should consider this dependence.
- Some months are missing due to fitting limitations; overall missing data is small but non-negligible for certain catchments.

## Inventory and accessibility
- HD_SSI_CatchInfo.csv provides a common reference for catchments and helps enable multi-sector planning.
- Data are designed to support cross-catchment drought analysis and comparability over time and space.
- The dataset is an outcome of the Historic Droughts Project (grant NE/L01016X/1) and is available via the project outputs and associated data centre references.

## Use cases and implications
- Enables analysis of UK hydrological drought characteristics at multiple time scales across numerous catchments.
- Facilitates cross-site comparisons and trend assessments using standardized, unitless SSI measures.
- Supports validation and development of drought management tools and planning across hydrometeorological and socio-economic sectors.

## References and acknowledgments
- Key methodological references include Vicente-Serrano et al. (2012), Svensson et al. (2017), Barker et al. (2016), and related SPI/SSI literature.
- Historic Droughts project and participating institutions are acknowledged; data referenced through NERC Environmental Information Data Centre and related outputs.