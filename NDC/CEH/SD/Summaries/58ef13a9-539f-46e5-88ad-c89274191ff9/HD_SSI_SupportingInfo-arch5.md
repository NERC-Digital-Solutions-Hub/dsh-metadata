# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

## Scope and content
- Dataset provides the Standardised Streamflow Index (SSI) for 303 UK catchments, a drought index based on the cumulative probability of monthly mean streamflow.
- SSI calculated for accumulation periods: 1, 3, 6, 9, 12, 18 and 24 months, assigned to the end of the accumulation period.
- Standard period for Tweedie distribution fitting: 1961-2010; covers 1891-2015.
- Data stored in CSV files; one file per catchment with SSI values for all accumulation periods.

## Project context and provenance
- Delivered from the Historic Droughts project (2014–2018; £1.5m), funded by UK Research Councils.
- Involves eight institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and the University of Oxford.
- An interdisciplinary effort to understand past UK droughts and improve drought management tools.
- SSI data derived from Historic Reconstructions of Daily River Flow for 303 UK Catchments (1891-2015); includes two naturalised model calibrations (making 305 daily series in total).

## Data and methods
- SSI calculated from modeled daily river flow series, aggregated to monthly means for 303 catchments (plus two naturalised calibrations).
- Fitted Tweedie distribution to each SSI time series for each accumulation period; transformed to Normal scores (mean 0, SD 1); SSI values are unitless.
- SSI values are truncated at +/-5 due to uncertainty at distribution tails.
- Acknowledges potential autocorrelation for accumulation periods >12 months due to overlapping data windows.
- Calibration performance: assessed using multiple metrics; NSE values are provided for the calibration period (1982-2014) and are available per catchment.
- Data limitations: use of modeled reconstructions; some catchments are near-natural or artificially influenced; users should assess data quality for specific applications.

## Data format and file structure
- Data format: CSV files; six SSI accumulation period columns (1, 3, 6, 9, 12, 18, 24 months) per catchment.
- File naming: HD_SSI_<Catchid>_189101-201511.csv (one file per catchment; 305 files for 303 catchments due to additional series).
- Missing data: indicated with -999. Missingness occurs at the start of each accumulation-period series and in other months where fitting the Tweedie distribution was not possible.
- Start months and counts of initial missing values by accumulation period are documented (e.g., 1-month series start Jan 1891 with 0 missing; 3-month series start Mar 1891 with 2 missing; etc.).
- For two catchments (31023 West Glen at Easton Wood and 39017 Rey at Grendon Underwood), the Tweedie distribution could not be fitted for any calendar month; extensive missing data recorded.
- Summary of missing data across catchments is provided in Tables 2 and 3; combined totals at the dataset level include 1575 missing values for catchment 31023 and 625 for 39017, plus 64 additional missing values across other catchments and accumulation periods.

## Catch information and metadata
- HD_SSI_CatchInfo.csv provides catchment-level metadata:
  - Catchid, NRFACatchmentName, Area_sqkm
  - Nested (whether catchment is within a larger catchment)
  - UKBN2_LFBN (UK Benchmark Network suitability for low-flow analysis)
  - NRFA_StationPage (URL to NRFA station page)
- Catch information supports discovery and cross-referencing with NRFA records.

## Data quality, limitations, and stewardship notes
- Data are based on modeled daily river flows; quality varies by catchment and calibration period.
- Overlapping data for accumulation periods >12 months can induce autocorrelation; results should be interpreted with this caveat.
- Large amounts of missing data exist for two catchments; users should assess suitability for analysis in those cases.
- Missing values are documented; some periods simply lack fitting data across catchments.
- All data and related references are anchored to the Historic Droughts project outputs; proper citation is required when used.

## Usage and applicability considerations for Data Stewards
- Ensure metadata completeness: link each HD_SSI_<Catchid> CSV to corresponding HD_SSI_CatchInfo.csv entry; preserve NRFA identifiers and URLs.
- Maintain data quality checks: verify NSE-based calibration notes per catchment; document any catchments with limited or missing SSI data.
- Governance of provenance: retain provenance notes about the modeling reconstructions (Smith et al., 2018) and the Historic Droughts project context; include citations for methods (Tweedie fitting, SCI/R packages) and related groundwater/flow references.
- Data access and reuse: acknowledge the 2014–2018 Historic Droughts project and associated funding; provide clear guidance on how to handle missing data and autocorrelation when applying SSI in drought assessment or policy planning.
- Versioning and updates: given the historical nature of the data (1891–2015), updates are unlikely; however, any future revisions should be versioned and accompanied by updated catchment metadata and NSEs.

## References and supporting materials
- Barker et al. (2016); Svensson et al. (2017); Dunn (2014); Gudmundsson & Stagge (2014).
- Smith et al. (2018); Tanguy et al. (2015, 2017); Vicente-Serrano et al. (2012).
- Historic Droughts project documentation and the NERC EIDC data records.