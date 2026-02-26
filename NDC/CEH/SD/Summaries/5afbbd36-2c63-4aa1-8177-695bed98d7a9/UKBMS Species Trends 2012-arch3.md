# UK Butterfly Monitoring Scheme (UKBMS) Methodology

- This document outlines the UKBMS approach to environmental health monitoring: standardized design, data collection, analysis, quality control, and data storage to measure butterfly abundance and trends across the UK. It demonstrates a structured monitoring framework with explicit measures, data governance, and reporting outputs.

## Experimental design/sampling regime
- Data are collected from over 1,000 sites annually across the UK.
- All-species transects: fixed-route line transect (2–4 km) sampled weekly from April to September; 5 m wide band; weather-conditional observations; transects fixed to enable year-to-year comparability; routes sampled for habitat/management representation; typically 26 counts per year.
- Data collection methods include all butterfly species along the transect, with some sites using single-species transects for focal species during limited periods.
- Timed counts and egg/larval web counts: targeted counts for specific species during designated periods; weather-conditional and time-bounded.

## Data collection methods
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free download) by recorders or regional transect coordinators.
- Regional coordinators compile data for their regions; Transect Walker files are uploaded to an Oracle database housing all records.

## Analytical methods
- Data validation occurs prior to analysis.
- Generalized Additive Models (GAMs) are used to impute missing values and compute site indices.
- Collated Indices: national annual indices for each species derived by combining site indices; use log10 transformation and scaling so the mean index across the series equals 2.
- Missing values across sites/years are estimated with a log-linear regression model to produce indices and trends.
- Trends are calculated as linear regressions on the collated indices:
  - across the whole series (1976–2012)
  - over the last 20 years (1993–2012)
  - over the last 10 years (2003–2012)
- Acknowledges that some species have shorter trend records due to insufficient data in early years.
- Past and current data updates can slightly alter previously reported trends as new data are integrated.

## Nature and units of recorded values
- Site indices are relative measures of population size, not absolute counts, and relate to other abundance measures (e.g., mark-release-recapture).
- Collated Indices are presented as the log10 of the Collated Index (LCI); trends are expressed as the slope of the Collated Index over time.
- Scaling ensures comparability across species; trends are interpreted by the slope and its statistical significance.
- The 20-year and 10-year trend metrics provide shorter-window perspectives on recent changes.

## Quality control
- Automatic validation within Transect Walker flags potential data entry errors (e.g., anomalous counts, out-of-flight-period records); recorders may adjust or confirm entries.
- Regional coordinators perform additional checks using their knowledge of sites.
- Further automated and manual validation steps check for: records outside known distributions, flight periods, first-time site records, extreme or unusual abundances.

## Format of stored data
- Species Trends are stored as CSV files.
- Key columns include:
  - Species, Common name, No.years
  - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
  - 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
  - 10-yr slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change
- Data are organized using standardized taxonomic references and metadata to support interpretation and reproducibility.