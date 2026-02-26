# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015) Barker, L.J., Smith, K.A., Svensson, C., Tanguy, M., Hannaford, J.

## Overview
- Dataset provides Standardised Streamflow Index (SSI) data for 303 UK catchments.
- SSI is a drought index based on the cumulative probability of monthly mean streamflow for a catchment.
- Calculations cover accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months, assigned to end-month.
- Time period: 1891–2015 (standardised distribution fit using 1961–2010 period).
- Data stored as CSV files; used in the Historic Droughts project (2014–2018).

## Data sources and methodology
- Based on modelled daily river flow for 303 catchments ( Historic Reconstructions of Daily River Flow for 303 UK Catchments, 1891–2015).
- SSI calculation: fit Tweedie distribution to 1-, 3-, 6-, 9-, 12-, 18-, 24-month accumulated flows; transform to standard normal distribution (mean 0, sd 1); values truncated at ±5.
- Relative to SPI, SSI values indicate drought (negative) or wetter-than-average periods (positive).
- For long accumulations, data overlap across time windows, leading to autocorrelation in SSI series.
- Calibration and model performance: NSE-based evaluation across catchments (1982–2014) used to select the best-performing ensemble run.

## Data format and availability
- File naming: HD-SI_<CatchmentID>-189101-201511.csv (one file per catchment/flow series; 305 files for 303 catchments).
- Columns: SSI accumulation periods (1, 3, 6, 9, 12, 18, 24 months) for each end-month.
- SSI values are normal scores (no units) in range -5 to +5.
- Missing data:
  - Represented by -999.
  - Start-month missing values vary by accumulation period (see Table 1 in the document).
  - Some catchments have substantial missing data (e.g., catchments 31023 and 39017).
  - Additional isolated missing values exist (see Table 3 and Appendix A1).
- Catchment metadata: HD_SSI_CatchInfo.csv includes Catchid, NRFA name, area, nesting flag, UK Benchmark Network flag, and NRFA station page link.

## Spatial and catchment context
- Catchments selected from NRFA boundaries; map-ready for GIS analysis.
- CatchInfo supports linking SSI data to catchment attributes and spatial boundaries for visualization and multi-criteria analysis.

## Data quality, caveats, and interpretation
- Data derived from modelled reconstructed daily flows; quality varies by catchment and period.
- Autocorrelation in SSI for long accumulation periods due to overlapping data windows; interpret rare/high-flow events with caution.
- Missing data may limit temporal coverage for certain catchments or accumulation periods; verify suitability for specific analyses.
- Standard period (1961–2010) used for Tweedie fitting to ensure consistency with SPI-based drought indicators.

## Practical GIS-focused notes
- Suitable for map-based drought monitoring and multi-catchment comparisons.
- Join SSI data to GIS boundaries via Catchid/NRFA identifiers; leverage HD_SSI_CatchInfo.csv for metadata and context.
- Use SSI ranges (-5 to +5) to visualize severity of drought or wet spells across space and time.
- Consider data quality flags and missing-value patterns when aggregating or performing trend analyses.

## Usage and references
- Context: Historic Droughts project (2014–2018), cross-disciplinary drought history and management tools.
- Key methods and related works:
  - SSI calculation and interpretation (Vicente-Serrano et al., 2012; Svensson et al., 2017).
  - Tweedie distribution for monthly streamflow aggregations (Dunn, 2014; Svensson et al., 2017).
  - Historic reconstructions of daily river flow data (Smith et al., 2018; in prep).
- Acknowledgement: Historic Droughts project, grant NE/L01016X/1.