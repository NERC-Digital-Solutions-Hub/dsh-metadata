# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- Two sampling sites in a rural South Lanarkshire dwelling: inside hall and outside garden.
- Garden backs onto grassland near a large dairy farm.
- Data collection and analysis conducted in 2022; dwelling owner handles site operator duties; Centre for Ecology and Hydrology (CEH) Edinburgh handles analysis.
- Sampling used CEH ALPHA® passive samplers with monthly exposure cycles.

## Sampling Method and Analysis
- CEH ALPHA® sampler: citric acid coated filter captures NH3; PTFE membrane protects filter with diffusion of NH3; membrane oriented downwards during exposure.
- Samplers mounted at ~1.5 m height on a shelter on a pole; replicates used for reliable estimates.
- Analysis: exposed samplers extracted into deionised water and analysed by SEAL AA3 using colorimetry; results converted to average NH3 concentration in air using uptake rate of 0.0038422 m3/h and exposure duration.
- Units: ammonia concentration reported as micrograms per cubic metre (µg NH3 m-3).

## Dataset and Structure
- Final dataset name: NH3_SouthLanarkshire_indoors_outdoors2022.csv.
- Data content: monthly data per site; each row represents one month for a site.
- Key columns (examples): site name, unique site identifier, network_id, parameter_id, exposure start/end dates and times, ammonia concentration, detection limit flag, verification status, data capture (%), validity flag, EMEP code, Month-Year.
- Concentrations are average values for the exposure period.

## Data Quality and Flags
- Data have quality flags and notes indicating concerns (referenced on page 4 of the source document).
- Quality rules:
  - Coefficient of variation (CV) < 15% across replicates; valid averages labeled as 103.
  - Values above calibration range may be valid if remeasurement isn’t possible due to issues.
  - Missing data or metadata are denoted by -9999 in the measurement field; prevents calculation.
- Common flags include:
  - 103: valid measurement with CV < 15%.
  - -9999: missing measurement or missing date/time metadata.
  - Various EMEP/data-status codes indicating data quality issues or special conditions (e.g., contamination, sampling anomalies, or invalid data).

## EMEP Flags and Metadata
- EMEP-related codes provide additional context on data status and data quality (e.g., contamination indicators, sampling anomalies, below-detection/over-range values, and missing data).
- Examples include 999 (data capture missing), 260 (contamination suspected), 653–659 (EMEP-related flags), 103 (valid CV-based flag), among others.
- Flags help assess data suitability for analysis and cross-network comparability.

## Site Information
- Inside site:
  - Start date: 01/01/17; End date: Ongoing.
  - Latitude: 55.64072; Longitude: 3.59705.
  - Height of air inlet above ground: 1.5 m.
  - Details: located in the hall of the dwelling.
- Outside site:
  - Start date: 01/01/17; End date: Ongoing.
  - Latitude: 55.64072; Longitude: 3.59705.
  - Height of air inlet above ground: 1.5 m.
  - Details: located in the garden of the dwelling.

## Data Use Considerations for Data Leaders
- Emphasizes a system-wide view: multiple sites, replicates, and detailed metadata to support data discovery and reuse.
- Replicates and QC rules are essential for reliable, policy-relevant conclusions.
- Rich metadata (dates, times, unit IDs, validity flags, and EMEP codes) supports traceability and interoperability with broader air-quality datasets.
- Potential data gaps to monitor: missing measurements (-9999), data capture gaps, calibration-range limitations, and contamination indicators that may affect comparability with other datasets.