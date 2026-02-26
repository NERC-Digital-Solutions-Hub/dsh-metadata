# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- Study at two CEH ALPHA passive samplers placed indoors (hall) and outdoors (garden) at a rural dwelling in South Lanarkshire.
- Garden backs onto grassland near a large dairy farm.
- Local site operator: dwelling owner; analysis: Centre for Ecology and Hydrology Edinburgh.
- Sampling performed in monthly cycles at the start of each month.

## Methods
- Passive sampling using CEH ALPHA samplers with a citric acid coated filter to capture NH3; a white PTFE membrane protects the filter.
- Membrane oriented downwards during exposure; samplers mounted about 1.5 m above ground.
- Replicates used to improve reliability; samples analyzed by SEAL AA3 using colourimetry to determine ammonium concentration.
- NH3 concentration in air calculated from ammonium concentration using the uptake rate of 0.0038422 m3 h-1 and exposure duration.
- Data flagged for concerns; details provided on data quality (see Data quality).

## Data structure and contents
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2022.csv.
- Each row represents one month of data for a single site (indoor or outdoor).
- Columns include: site name, unique site identifier, network_id, parameter_id (alpha_NH3_g), measurement start/end dates and times, concentration (µg NH3 m-3), detection flag, verification status, unit id (24 = µg NH3 m-3), data capture percentage, validity flag, and EMEP code.
- Concentrations are the average NH3 concentration for the specified exposure period.

## Data quality and flags
- Quality checks include:
  - Coefficient of variation (replicates) must be <15%; if >15%, evaluation to decide discard or keep; such datasets may be flagged (103).
  - Values above calibration range can be valid if re-measurement was not possible.
  - Missing data indicated by -9999 in relevant fields.
- Data are flagged to indicate concerns; final dataset includes these flags.
- Dataset includes EMEP data flags and accompanying meanings to aid interpretation (e.g., missing data, below detection limit, sampling anomalies, contamination indicators, etc.).

## Site information
- Inside (hall of dwelling): start_date 01/01/17; end_date ongoing; coordinates 55.64072, 3.59705; height of air inlet above ground 1.5 m; location: inside hall of dwelling.
- Outside (garden): start_date 01/01/17; end_date ongoing; coordinates 55.64072, 3.59705; height of air inlet above ground 1.5 m; location: garden of dwelling.

## Data availability and usage notes
- Data are organized with clear month-year granularity and include spatial identifiers to support trend analysis.
- Replicates and quality flags enable filtering for robust analysis and comparability with other datasets.
- Suitable for exposure assessment and correlation analyses, with attention to data capture, validity, and EMEP flag interpretations.

## Considerations for analysts
- Be mindful of data quality flags (CV, detection limits, contamination, sampling anomalies) when aggregating or comparing indoor vs. outdoor measurements.
- Use the month-level data to evaluate temporal patterns and potential indoor-outdoor differences.
- When integrating with other datasets, align site identifiers, coordinates, and EMEP flag semantics for consistent interpretation.
- Consider the potential implications of local farm activity and environmental context (grassland dairy farm) on outdoor NH3 concentrations.