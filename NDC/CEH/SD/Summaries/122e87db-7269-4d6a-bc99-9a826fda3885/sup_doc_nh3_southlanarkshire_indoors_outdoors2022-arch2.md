# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2022

## Overview
- Ammonia air concentrations measured at two sites (indoor hall and outdoor garden) of a rural dwelling in South Lanarkshire during 2022.
- Operation and data processing coordinated by Centre for Ecology and Hydrology Edinburgh (operator: dwelling owner; analysis: CEH Edinburgh).
- Data contribute to environmental monitoring with standardized reporting formats (monthly exposure periods; units: µg NH3 m-3).

## Study design and locations
- Sites: inside (hall of dwelling) and outside (garden area) the same dwelling.
- Location coordinates: 55.64072 N, 3.59705 W for both indoor and outdoor sites.
- Height of air inlets: 1.5 m above ground.
- Context: outdoor garden backs onto grassland adjacent to a large dairy farm.
- Monitoring timeline: ongoing since 01/01/2017; data for 2022 are summarized in the 2022 dataset.

## Sampling and analysis methods
- Instrument: CEH ALPHA® passive samplers with a citric acid coated filter to capture NH3; PTFE membrane protects the filter.
- Exposure setup: replicate samplers mounted on shelters on poles/posts at ~1.5 m height; single exposure period per month.
- Analysis: samplers extracted with deionised water; NH3 quantified by SEAL AA3 using colorimetry; results converted to ambient NH3 concentration using a known uptake rate (0.0038422 m³ h⁻¹) and exposure duration.
- Data recording: dataset includes monthly NH3 concentration for each site.

## Data processing and quality control
- Data qualification: raw data assessed against quality rules; flagged data highlight concerns.
- Key QC rules:
  - Coefficient of variation (replicates) < 15% otherwise assessed for discard or validity (flag 103 if average is representative).
  - Data beyond calibration range may be valid if remeasurement is not possible due to instrument failure.
  - Missing measurements or metadata are indicated by -9999 for concentration or meta fields.
- Data flags: comprehensive data-status codes (including verification status, data capture, and EMEP flags) accompany each row; details are aligned with EMEP flag definitions (e.g., missing data, below detection limit, sampling anomalies, contamination).

## Dataset contents and data fields
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2022.csv.
- Structure: one row per site per month; columns include:
  - Site name; unique site identifier; network_id (RSW)
  - Parameter type (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Measured NH3 concentration (units: µg NH3 m⁻³)
  - Data quality flags (e.g., -9999 for missing)
  - Verification status (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
  - Data capture percentage; validity flag (1 = valid, -1 = not valid)
  - EMEP status code and associated flags
  - Month-Year (mmm-yy)

## Site details
- Indoor site:
  - Location: hall of dwelling
  - Start date: 01/01/17; End date: Ongoing
  - Coordinates: 55.64072, -3.59705
  - Inlet height: 1.5 m
- Outdoor site:
  - Location: garden of dwelling
  - Start date: 01/01/17; End date: Ongoing
  - Coordinates: 55.64072, -3.59705
  - Inlet height: 1.5 m

## Data interpretation and usage
- The dataset provides monthly ambient NH3 concentrations for indoor and outdoor environments at a single rural dwelling, enabling assessment of environmental health relative to standards and policy performance over time.
- Flags and metadata enable assessment of data quality, replication reliability, and any contextual data issues (e.g., contamination or sampling anomalies).

## Data availability
- Data are stored and shareable via the standard monitoring portals used for UK environmental data.
- Documentation of data flags and EMEP status codes is referenced to additional resources (e.g., nilu.no) for interpretation.