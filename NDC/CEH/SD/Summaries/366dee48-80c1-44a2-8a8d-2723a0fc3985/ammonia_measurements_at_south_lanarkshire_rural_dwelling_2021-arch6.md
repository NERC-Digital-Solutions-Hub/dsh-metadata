# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

## Overview
- Study measuring ammonia (NH3) concentrations at two sites in a rural dwelling in South Lanarkshire: inside (hall) and outside (garden).
- Conducted using UKCEH ALPHA® passive samplers; analysis performed by Centre for Ecology and Hydrology Edinburgh.
- Samplers exposed in monthly cycles; indoor and outdoor data collected from 2017 onward, with a final dataset covering 2019–2020 in the reported file and 2021 in the document title.
- Data intended to support assessment of NH3 in air and facilitate self-serve exploration of concentrations and trends.

## Study design and sampling sites
- Two sites at a single dwelling:
  - Inside: located in the hall, 1.5 m above ground, coordinates 55.64072, -3.59705.
  - Outside: located in the garden, directly backing onto grassland (dairy farm), same height and coordinates as inside.
- Replicate samplers deployed at each site to improve reliability.
- Exposure period: monthly cycles beginning at the start of each month.
- Site operator duties performed by the dwelling owner; analysis conducted by UKCEH.

## UKCEH ALPHA® sampler method
- Passive sampler uses a citric acid coated filter to capture NH3; protected by a white PTFE membrane positioned to diffuse NH3 during exposure.
- Sampler mounted on a shelter on a pole at ~1.5 m height above ground.
- After exposure, samplers are extracted into deionised water and analyzed by SEAL AA3 using colorimetric detection to quantify ammonium.
- NH3 concentration in air (µg NH3 m-3) calculated from the measured ammonium concentration using a known sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Raw data include quality flags and are described in accompanying pages (e.g., page 4 for data flags).

## Data processing and quality assurance
- Data are quality checked with predefined rules:
  - Rule 1: Coefficient of variation (CV) among replicates < 15%; if CV > 15%, evaluated for potential discard of replicates; if representative, data flagged as valid (103).
  - Rule 2: Data above calibration range may be valid if remeasurement isn’t possible due to instrument failure or sample loss.
  - Rule 3: Missing data indicated by -9999 (or missing date/time metadata), preventing concentration calculation.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv, containing accepted values with appropriate flags.
- Data capture and validation status are embedded within the data flags (e.g., Verified, Preliminary Verified, Not Verified).

## Data content and structure
- Each row represents one month of data for a single site.
- Columns include:
  - Site id and Site name
  - Network id (RSW)
  - Parameter id (alpha_NH3_g)
  - Measurement start date/time and end date/time
  - Measurement (ammonia concentration in µg NH3 m-3)
  - Less than flag (indicates values below detection limit of 0.03)
  - Verification id (0–3 indicating verification status)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity id (1 = valid, -1 = not valid)
  - EMEP code and EMEP flags
  - Month-Year (MMM-YY)
  - Comments on data
- Spatial identifiers for site locations are provided, with site-specific details on page 5 in the source document.

## Data quality flags and interpretation
- EMEP flags and data status codes provide context for data quality and any caveats:
  - Example interpretations:
    - 103: CV of replicate ALPHA samplers > 15%; valid measurement.
    - 999: Data capture indicator or missing data; missing measurement.
    - 781/780, 654/653: Values near or above/below limits with notes on validity or representativeness.
    - 653/652/651, etc.: Indicate potential local influences (e.g., construction, agricultural activity, traffic) and their impact on validity.
  - Flag meanings are defined in the accompanying EMEP flag documentation referenced in the dataset.

## Site information and geography
- Inside site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: -3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the hall of the dwelling
- Outside site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: -3.59705
  - Height of air inlet: 1.5 m
  - Details: Located in the garden of the dwelling
- Both sites share the same coordinates, reflecting their close proximity to the dwelling and surrounding grassland/dairy farm environment.

## Data availability and notes
- The final dataset contains monthly NH3 concentrations for each site, with data quality and flag metadata to assess reliability.
- Data collection is linked to UKCEH ALPHA samplers and standard analysis protocol; ongoing sampling at the dwelling since 2017.
- Users should note potential discrepancy between the document title (2021) and the dataset content (2019–2020) and refer to the source pages for clarification on time period coverage and any updates.