# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

## Project and purpose
- Four-year Historic Droughts project (2014–2018; £1.5m) funded by UK Research Councils to understand past UK droughts and develop tools for managing droughts.
- Involves eight UK institutions (British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, University of Oxford).
- Goal: develop an interdisciplinary understanding of drought from hydrometeorological, environmental, agricultural, regulatory, social, and cultural perspectives; provide a common reference for policy makers, regulators, water suppliers, agriculture, and industry.
- Data product supports cross-sectoral understanding and planning for drought/water scarcity events.

## Data content and scope
- Standardised Streamflow Index (SSI) data for 303 UK catchments; drought index based on the cumulative probability of monthly mean streamflow for a catchment.
- Accumulation periods: 1, 3, 6, 9, 12, 18 and 24 months; SSI values assigned to the end-month of each accumulation period.
- Standard period used to fit the Tweedie distribution: 1961–2010 (to align with SPI data from the project).
- Temporal coverage: 1891–2015; units are normal scores (dimensionless) with mean 0 and standard deviation 1; SSI values capped at -5 and +5 due to extremes.
- Data derived from modelled daily river flow reconstructions (Historic Reconstructions of Daily River Flow for 303 UK Catchments, 1891–2015), with some catchments also having naturalised flow calibrations; 305 daily series considered in total (NRFA catchment IDs augmented for naturalised calibrations where applicable).
- Output data are stored as CSV files, one per catchment, with seven accumulation-period columns (1, 3, 6, 9, 12, 18, 24 months).

## Data source, method, and interpretation
- SSI calculation follows Vicente-Serrano et al. (2012): fit a Tweedie distribution to monthly-aggregated streamflow for each accumulation period, transform to Normal scores, and derive the SSI.
- Note: negative SSI indicates below-average flows (drought), positive SSI indicates above-average flows.
- Methodological details:
  - Based on best-performing model run from the ensemble of daily streamflow reconstructions (calibrated to naturalised flow where available).
  - Calculations performed on monthly means, with aggregation period overlapping data for longer accumulation periods, introducing autocorrelation in SSI series.
  - Data are national-scale UK-focused and aligned with SPI-based drought indicators used elsewhere in the Historic Droughts project.
- Cautions:
  - SSI series for accumulation periods > 12 months share data across overlapping windows, violating independence assumptions for standard frequency analysis.
  - Autocorrelation and data overlap may affect interpretation of long-duration drought signals.

## Data format and file organization
- File format: CSV; naming convention: HD_SSI-CatchmentID-189101-201511.csv (one file per catchment; 305 files covering 303 catchments).
- Contents:
  - Columns correspond to accumulation periods, labeled by the number of months (1, 3, 6, 9, 12, 18, 24).
  - Values are SSI normal scores (mean 0, sd 1), without units, range -5 to +5 (with truncation at extremes).
  - Missing data indicated by -999.
  - Start month/year and the number of initial -999 values are specified per series (Table 1 in the document); some catchments have larger gaps (Table 2).
  - Additional isolated missing values exist in a small number of cases (Table 3).
- Catchment metadata:
  - HD_SSI_CatchInfo.csv lists catchment details: Catchid, NRFACatchmentName, Area_sqkm, Nested, UKBN2_LFBN, NRFA_StationPage.
- Data provenance:
  - Based on Historic Reconstructions of Daily River Flow for 303 UK Catchments (1891–2015) by Smith et al. (2018; in prep); includes calibration NSE metrics over 1982–2014.
- Acknowledgement: dataset outcome of the Historic Droughts Project (grant NE/L01016X/1).

## Data quality, gaps, and caveats
- Missing data:
  - Table 1 documents start-month and initial missing values for each accumulation period (ranges from 0 to 12+ values at start).
  - Table 2 reports substantial missing values for two catchments (31023 and 39017) across multiple months; totals indicate 1575 missing values for 31023 and 625 for 39017, with some months entirely missing for those catchments.
  - Table 3 lists additional isolated missing values affecting 35–42 catchments depending on accumulation period.
  - Overall, 64 additional missing values not explained by Tables 2–3 are documented (Appendix Table A1).
- Data similarity and notes:
  - SSI is calculated from modelled streamflow reconstructions; readers should assess data suitability for their specific use case.
  - For long accumulation periods, overlapping data windows create potential autocorrelation; this should be considered in analyses that assume independence.

## Usage and applications
- Designed to support cross-sector drought planning and policy-making by providing a consistent, multi-catchment, multi-timescale drought indicator.
- Useful for retrospective drought analysis, trend assessment, and cross-referencing with hydrometeorological indicators and socio-economic drivers of drought impacts.
- Metadata and catchment-level information facilitate data discovery, discoverability, and integration with other NRFA/NERC datasets.

## References and acknowledgement of sources
- Primary references include work on drought indicators (SPI/SSI), UK drought characteristics, and the supporting data sets and calibration studies cited in the document.
- Funding and collaboration acknowledged through the Historic Droughts Project and participating institutions.