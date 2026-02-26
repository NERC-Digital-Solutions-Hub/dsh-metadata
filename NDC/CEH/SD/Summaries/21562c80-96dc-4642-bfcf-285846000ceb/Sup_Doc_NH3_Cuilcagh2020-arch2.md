# Sup_Doc_NH3_UWT_Cuilcagh

## Overview and purpose
- Measurements near Cuilcagh (Ireland and Northern Ireland) to observe local ammonia (NH3) impacts on vegetation.
- Operator: Ulster Wildlife Trust (site duties); Analysis: UK Centre for Ecology and Hydrology Edinburgh (CEH).
- Monitoring cadence: monthly exposure cycles; replicates used to improve reliability.

## Methods and instrumentation
- Passive sampling with UK CEH ALPHA® samplers.
- Sampling setup: citric acid coated filter to capture NH3; PTFE membrane protects filter; membrane oriented facing downward during exposure.
- Exposure: samplers mounted ~1.5 m above ground on shelters, with triplicate samplers per site.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry; results converted to average NH3 concentration in air using a known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data flags: data quality concerns flagged; details provided in accompanying pages.

## Data quality assurance and processing
- Raw data quality checks:
  - Coefficient of variation (CV) of replicates must be < 15% for reliability; if >15%, replicates may be discarded or flagged; valid data may still be retained with a 103 flag.
  - Some samples reported above calibration range but considered valid due to limited options for rerun.
  - Missing data or metadata (denoted as -9999) lead to non-calculable concentrations.
- Final dataset: NH3_Cuilcagh2020.csv containing accepted NH3 values with appropriate flags.
- Units: NH3 concentration in air expressed as micrograms per cubic metre (µg NH3 m-3).
- Data structure notes: rows correspond to one month of data for a single site; columns include site name, unique site identifier, network_id, parameter_id, start/end dates and times, exposure period, ammonia concentration, data qualifiers, verification status, unit, data capture, validity, and EMEP status.

## Data structure and flags
- Key columns (examples):
  - Station name, unique site identifier, network_id (RSW), parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times; exposure period
  - Ammonia concentration (µg NH3 m-3)
  - Less than flag (detection limit)
  - Verification id (Not verified, Preliminary verified, Verified)
  - Unit id (µg NH3 m-3), Data capture (%), Validity_id (valid/not valid)
  - EMEP code (data status flags), Month-Year, Comments
- EMEP flags cover data quality and contextual notes (e.g., below detection limit, contamination, sampling period variability, nearby emissions, etc.), with predefined numeric codes and meanings.

## Site information and layout
- Sites monitored (with coordinates and sampling height 1.5 m):
  - Boardwalk: 54.218694, -7.823424
  - Eshvagh: 54.190490, -7.846421
  - Corcashel: 54.187536, -7.973599
  - Grouse Project: 54.130905, -7.896038
  - Shridrinagh: 54.119063, -7.995085
- Monitoring began 01/02/2020 and continuing (ongoing) for all sites.
- Data capture and site metadata are included in the final dataset and related documentation.

## Dataset description and accessibility
- Final dataset: NH3_Cuilcagh2020.csv
- Content: monthly NH3 concentration values per site, with associated metadata and quality flags.
- Data storage and sharing: datasets are stored and uploaded to appropriate portals to enable external access and reuse.

## Relevance to the Analysts Monitoring the Environment archetype
- Data are produced using standardized, established methods, enabling cross-site and temporal comparisons.
- Emphasis on data verification, quality assurance, and clear data flags aligns with standardised environmental health outputs.
- Datasets are designed for reuse beyond initial outputs, supporting broader environmental health and policy performance scrutiny.
- Data accessibility objectives are addressed by storing and enabling access to both the final outputs and underlying data.