# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

## Overview
- Provides Standardised Streamflow Index (SSI) data for 303 UK catchments to monitor hydrological drought and variability.
- SSI is a drought index based on the cumulative probability of monthly mean streamflow for each catchment, enabling cross-time and cross-catchment comparisons.
- Data span: 1891–2015; standard period for distribution fitting: 1961–2010; six accumulation periods plus 1, 3, 6, 9, 12, 18, and 24 months.
- Aims to support understanding and management of drought and water scarcity, aligning hydrological indicators with socio-economic and regulatory contexts.

## Data & methods for monitoring
- Source dataset: Historic Reconstructions of Daily River Flow for 303 UK Catchments (1891–2015); modelled daily flows calibrated to naturalised flows, using the best-performing ensemble run.
- SSI calculation:
  - For each catchment and accumulation period, monthly flows are fit to a Tweedie distribution (lower bound zero) using the standard period 1961–2010.
  - Data are transformed to Normal scores (mean 0, sd 1); SSI values are unitless and truncated at ±5 due to extreme-value uncertainty.
  - SSI accumulation period end-months are assigned (e.g., SSI-6 for the end of July 1998 corresponds to Feb–Jul 1998).
- Methodological notes:
  - Uses the SCI package in R with a custom function to incorporate the Tweedie distribution.
  - For accumulation periods >12 months, overlapping data cause autocorrelation; SSI values reflect relative rarity/severity within the same duration, but underlying data are not independent.
  - Acknowledges potential autocorrelation and dataset limitations when interpreting long-duration drought signals.

## Data structure, format & access
- Data organization:
  - One .csv per catchment/flow series; 305 series in total (covering 303 catchments with some catchments having multiple calibrations).
  - Files contain SSI values for accumulation periods: 1, 3, 6, 9, 12, 18, and 24 months; values are normal scores in the range -5 to +5.
  - Missing data indicated by -999; start months and counts of initial missing values are provided per accumulation period.
- Key metadata:
  - HD_SSI_CatchInfo.csv provides catchment-level metadata:
    - Catchid, NRFACatchmentName, Area_sqkm, Nested flag, UKBN2_LFBN flag, NRFA_StationPage URL.
- Data provenance and accessibility:
  - Data derived from Historic Droughts project; acknowledgments and references included.
  - HD_SSI_CatchInfo.csv links to NRFA station pages for catchment context.
  - Dataset publicly released through the NERC Environmental Information Data Centre (EIDC) as part of Historic Droughts outputs.

## Data quality, uncertainty & limitations
- Data quality considerations:
  - SSI derived from modelled reconstructed daily flows; calibration assessed with NSE metrics (1982–2014 period); users should review catchment-specific quality via Smith et al. (2018).
  - Some catchments exhibit substantial missing data for certain months; two catchments (31023, 39017) have extensive, sustained data gaps.
  - For some months, Tweedie distribution could not be fitted; additional missing values exist (across several catchments and accumulation periods).
- Limitations for interpretation:
  - Autocorrelation inherent in long accumulation periods due to overlapping data windows.
  - Missing data and potential quality issues in certain catchments may affect comparability across all 303 catchments.
  - SSI values are unitless normal scores; comparisons rely on standardized scope rather than physical units.

## Metadata, governance & reproducibility
- Metadata availability:
  - Comprehensive per-catchment metadata in HD_SSI_CatchInfo.csv; start months and missing value counts documented in accompanying tables.
- Data governance:
  - Data are produced with explicit standardisation (1961–2010 Tweedie fitting period) to align with SPI-based drought indicators; data sharing and clear provenance support transparent governance.
- Reproducibility:
  - Calculation workflow (monthly aggregation, Tweedie fitting, normal-score transformation) documented; software references include the SCI and tweedie R packages and Smith et al. (2018) foundational work.

## Practical use for monitoring frameworks
- Cross-catchment drought surveillance:
  - Enables comparative drought assessment across 303 UK catchments over more than a century.
  - Supports multi-decadal monitoring, scenario evaluation, and policy analysis within water resource management frameworks.
- Monitoring outputs:
  - Facilitates dashboards and reports with standardized drought indicators, enabling consistent communication to stakeholders.
- Integration with broader drought tools:
  - Aligned with SPI-based approaches and the Historic Droughts Inventory for multi-sectoral understanding of drought drivers and responses.

## References & provenance notes
- Core references for methodology and data provenance include Barker et al. (2016), Svensson et al. (2017), Tanguy et al. (2015, 2017), Vicente-Serrano et al. (2012), and Smith et al. (2018, in prep).
- Acknowledges Historic Droughts project (grant NE/L01016X/1) and Public data releases via NRFA/NERC EIDC.