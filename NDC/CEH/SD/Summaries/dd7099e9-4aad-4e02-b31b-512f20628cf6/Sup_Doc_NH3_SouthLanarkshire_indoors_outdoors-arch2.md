# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Two monitoring sites in rural South Lanarkshire: indoor hall of a dwelling and outdoor garden of the same dwelling.
- Garden backs onto dairy farm grassland.
- Local site operator: dwelling owner; analysis: Centre for Ecology and Hydrology Edinburgh.
- Purpose: measure ammonia (NH3) concentrations in air on a monthly cycle to support environmental health monitoring.

## Measurement Methodology
- Instrument: CEH ALPHA® passive samplers with citric acid–coated filters and PTFE membranes.
- Deployment: replicates at about 1.5 m above ground on shelter posts; exposure at the start of each month.
- Analysis: exposed samplers extracted with deionised water and analyzed by SEAL AA3 (colorimetry) to determine ammonium concentration.
- Conversion: ammonium concentration converted to average NH3 concentration using a known uptake rate of 0.003241315 m3 h−1 and exposure duration.
- Output units: micrograms NH3 per cubic metre of air (µg NH3 m−3).
- Replication: multiple samplers per site to improve reliability.

## Data Structure and Quality Assurance
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors.csv, with one row per month per site and columns including site name, exposure period dates, NH3 concentration, and a data flag.
- Data flags: indicate quality concerns; flag meanings and handling described (details in dataset and accompanying documentation).
- Quality rules:
  - Coefficient of variation (CV) of replicates must be < 15% for data to be considered representative; if >15%, replicates reviewed and may be discarded; valid data can still be retained with a 103 flag.
  - Values above calibration range may be reported and still treated as valid if re-analysis was not possible due to instrument issues.
  - Missing data indicated by -9999 (e.g., missing measurement or missing meta data required to calculate concentration).
- Dataset content:
  - Each row corresponds to one month’s data for a single site.
  - Columns include: site name, network_id, parameter_id, measurement start/end dates and times, concentration, below-detection flag, verification id, unit id, data capture percentage, validity id, EMEP code, and Month-Year.
- EMEP flags: extensive flag codes (e.g., data capture status, validity, reasons for unusual values) with predefined meanings (e.g., contamination, near-field influences, detection limits, sampling period anomalies).

## Site Information and Metadata
- Inside site:
  - Start: 01/01/17; End: Ongoing; Latitude 55.64072, Longitude 3.59705; Inlet height: 1.5 m; Location: hall of dwelling.
- Outside site:
  - Start: 01/01/17; End: Ongoing; Latitude 55.64072, Longitude 3.59705; Inlet height: 1.5 m; Location: garden of dwelling.

## Data Management and Accessibility
- Data are stored and uploaded to the appropriate portals to support ongoing monitoring and accessibility.
- Emphasis on reusing and combining NH3 data with other relevant datasets to enhance the value of monitoring efforts rather than keeping outputs as standalone products.

## Relevance for Analysts Monitoring the Environment
- Uses standardized sampling and QA procedures to enable consistent, time-series assessment of environmental health.
- Provides clear metadata and flagging to support scrutiny, reproducibility, and integration into broader environmental health analyses.
- The inclusion of replicate samplers and detailed data-status codes supports transparent assessment of data quality and policy-relevant monitoring over time.