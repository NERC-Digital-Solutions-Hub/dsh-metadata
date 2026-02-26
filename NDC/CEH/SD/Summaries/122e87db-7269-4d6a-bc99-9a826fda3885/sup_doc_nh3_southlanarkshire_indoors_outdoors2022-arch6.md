# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- A paired indoor (hall) and outdoor (garden) ammonia monitoring study at a rural dwelling in South Lanarkshire during 2022.
- Local site operator: dwelling owner; analysis conducted by the Centre for Ecology and Hydrology (CEH) Edinburgh.
- Passive CEH ALPHA® samplers deployed monthly, with replicate samplers to improve reliability.

## Method: CEH ALPHA® sampler procedure
- Sampler design: citric acid coated filter to capture NH3; protected by a white PTFE membrane positioned facing downwards; exposure at about 1.5 m above ground.
- Replication: multiple samplers per site to enhance reliability.
- Analysis: exposed samplers extracted into deionised water; NH3 measured by SEAL AA3 colorimetry; results converted to average NH3 in air using a known uptake rate of 0.0038422 m3 h-1 and exposure duration.
- Output: final concentration in air reported as µg NH3 m-3 for each monthly exposure period.
- Data handling: data flagged for quality concerns (see Data quality section); dataset named NH3_SouthLanarkshire_indoors_outdoors2022.csv.

## Data structure and contents
- Dataset: NH3_SouthLanarkshire_indoors_outdoors2022.csv
- Granularity: monthly data per site (indoor and outdoor); two sites per dwelling.
- Key fields (examples):
  - Station name / unique site identifier; network_id (RSW)
  - Parameter_id (alpha_NH3_g)
  - Measurement start date/time and end date/time (exposure period)
  - Measurement (ammonia concentration in µg NH3 m-3)
  - Less than (detection limit flag; 1 if below detection limit)
  - Verification id (1: Verified; 2: Preliminary verified; 3: Not verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture (percentage)
  - Validity_id (1 = valid; -1 = not valid)
  - EMEP code (data status flags)
  - Month-Year (MMM-YY)
- Data content notes: rows correspond to one month of data per site; sites listed with spatial identifiers; units standardized to µg NH3 m-3.

## Data quality and flags
- Quality checks:
  - Coefficient of variation (CV) of replicates must be < 15% for data to be considered representative; CV > 15% leads to evaluation of replicates and potential exclusion.
  - Some samples may exceed the calibration range but remain valid if still interpretable.
  - Missing data or meta data coded as -9999.
- Data status / flags (EMEP framework):
  - 103: CV of replicates ≤ 15%; valid measurement
  - 999: data capture missing; data considered missing
  - 781: value below detection limit; reported as detected value
  - 780: below detection or quantification limit; estimated/valid value
  - 654 / 653 / 652 / 651 / 660 / 770 / 659: various contextual flags (e.g., sampling period longer/shorter than normal, nearby influences such as agricultural activity, contamination, etc.)
- Data capture and validity indicators accompany each record to aid data quality assessment.

## Site information
- Inside
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the hall of the dwelling
- Outside
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the garden of the dwelling

## Relevance for data support
- The dataset provides a structured, QA-annotated time series of indoor and outdoor ammonia concentrations suitable for cross-site comparisons, trend analyses, and integration with other environmental or agricultural data.
- Clear documentation of measurement methodology, units, replication strategy, and data quality flags supports traceability, data cleaning, and robust self-service analytics (e.g., dashboards, pivot-style summaries).
- The standardized data fields (site, period, concentration, flags, and metadata) facilitate data merging with other monitoring campaigns and policy-relevant reporting initiatives.