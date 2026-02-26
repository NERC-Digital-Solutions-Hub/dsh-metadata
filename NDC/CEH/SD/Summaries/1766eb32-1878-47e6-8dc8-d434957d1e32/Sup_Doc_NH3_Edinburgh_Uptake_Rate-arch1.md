# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Report of initial results to determine the uptake rate for CEH ALPHA® samplers used to measure ammonia (NH3) in air for the UK and similar climates.
- Sampling conducted by UK CEH Edinburgh and AFBI Hillsborough; analysis by CEH Edinburgh.
- Data for the first year were not used for uptake-rate calculations due to COVID-19 data losses.

## Sampling Method and Analysis
- Passive ALPHA® samplers with citric acid coated filter to capture NH3; a white PTFE membrane protects the filter.
- Membrane faces downward during exposure; samplers mounted ~1.5 m above ground on shelters.
- Replicates used per site to improve reliability.
- Analysis: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetry (ammonium).
- NH3 concentration in air is derived from measured ammonium using a known uptake rate of 0.003241315 m3 h-1 and exposure duration.

## Data Quality and Flagging
- Data flagged to highlight concerns (details on data quality in accompanying pages).
- Quality rules for raw data:
  - Coefficient of variation (CV) of replicates must be < 15%; if >15%, evaluate replicates and possibly exclude; otherwise data considered valid with flag 103.
  - Values above calibration range may be valid if not rerunnable due to instrument issues.
  - Missing data indicated by -9999 in measurement or meta-data fields.
- Final dataset: NH3_Edinburgh_Uptake_Rate_2020.csv containing accepted data values with appropriate flags.
- Data status fields include verification status, data capture percentage, and EMEP status codes (detailed flag mappings provided).

## Dataset Contents and Fields
- Each row represents one month of data for a single site.
- Core fields:
  - Site name and unique site identifier
  - Network_id (RSW)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (units: µg NH3 m-3)
  - Data quality flags: less than detection flag, verification id, unit id (µg NH3 m-3), data capture percentage, validity id (1 = valid, -1 = not valid), EMEP code, Month-Year, Comments
- Concentrations are reported as average NH3 concentration for the exposure period.

## EMEP and Data Flags (Key Points)
- Data capture and validity codes (examples):
  - 103: CV of replicate ALPHA samplers > 15%; considered valid
  - 781/780: values below detection limit or below quantification limit, but reported as valid
  - 999, 260, 553, 559, etc.: various data-capture and contamination/local influence notes
- Data status fields help interpret data quality and any caveats for each record.
- EMEP flags provide additional metadata about data status and quality checks.

## Site Information
- Edinburgh uptake rate OTC sites started 01/03/2020; ongoing.
  - Coordinates and height above ground: ~1.5 m
  - Collocated with UKEAP UKA00128
- Auch site: started 01/03/2020; ongoing; coordinates provided; height 1.5 m
  - Collocated with UKA00451
- Hills site: started 01/03/2020; ongoing; coordinates provided; height 1.5 m
  - Collocated with UKA00293

## Notes on Data Use and Accessibility
- The dataset provides a structured, replicable basis for estimating NH3 air concentrations using ALPHA samplers.
- Emphasizes data traceability: site names, unique identifiers, network IDs, measurement metadata, and detailed quality flags are included to support reproducibility and quality assessment.
- The 2020 dataset represents accepted measurements; a first-year uptake-rate determination was not performed due to data losses in the COVID-19 period.