# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Two sites in a rural area of South Lanarkshire measuring ammonia (NH3) in air: one indoors (hall of dwelling) and one outdoors (garden of dwelling).
- Sampling and analysis conducted by Centre for Ecology and Hydrology (CEH) Edinburgh; operator duties by dwelling owner.
- Data collection uses CEH ALPHA® passive samplers, with monthly exposure cycles starting at the beginning of each month.
- Location features: garden backs onto grassland that is part of a large dairy farm.

## Sampling and Analytical Method
- Samplers: CEH ALPHA® passive samplers with citric acid coated filter to capture NH3; PTFE membrane protects the filter; membrane oriented downwards during exposure; samplers mounted on a shelter on a pole ~1.5 m above ground.
- Replication: multiple samplers per site to improve reliability.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetry (ammonium refers to NH3 measurement after uptake); concentration in air calculated using the sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Data outputs: final dataset named NH3_SouthLanarkshire_indoors_outdoors.csv; results expressed as average NH3 concentration in air (µg NH3 m-3) over the specified exposure period.

## Data Structure and Quality Flags
- Each row represents one month of data for a single site.
- Columns include: site name, unique site identifier, network_id, parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration (µg NH3 m-3), flag for value below detection, verification status, unit id (24 = µg NH3 m-3), data capture percentage, validity status, EMEP code, and Month-Year.
- Data flags and quality controls:
  - CV of replicates < 15% used to validate replicates; if CV > 15%, replicates may be discarded or notes added; data may be flagged as valid (103) if the average is representative.
  - Some samples exceed the calibration range but are still considered valid due to instrument limitations and inability to re-run.
  - Missing data coded as -9999 for the measurement variable or metadata.
- EMEP flags provide context on data status and potential issues (e.g., detection limit, contamination, proximity influences, etc.). A range of specific codes indicates reasons such as below detection, contaminated samples, or nearby sources.

## Site Details
- Inside site:
  - Start: 01/01/17; End: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Location detail: Located in hall of dwelling
- Outside site:
  - Start: 01/01/17; End: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Location detail: Located in garden of dwelling

## Context for Analysis and Interpretation
- Proximity to agricultural activity (grassland on a large dairy farm) suggests potential agricultural NH3 sources influencing outdoor measurements.
- Indoor and outdoor measurements allow assessment of NH3 concentration gradients and potential indoor infiltration relative to outdoor levels.
- Data are monthly and at a local (site-specific) scale; replication and QA procedures support robust interpretation, though data gaps or scale limitations may apply when aggregating or comparing with other datasets.

## Data Access and Notes for Analysts
- The dataset structure and quality flags are designed to support filtering for valid measurements and understanding data limitations.
- Details on data flags and QA decisions are noted (e.g., page references for data quality explanations in the source documentation).