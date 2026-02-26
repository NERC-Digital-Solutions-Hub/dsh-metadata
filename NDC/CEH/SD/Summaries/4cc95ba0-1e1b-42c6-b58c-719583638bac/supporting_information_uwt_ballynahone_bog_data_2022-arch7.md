# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Overview
- A transect of sampling sites across Ballynahone National Park (an ASSI/SAC and Ramsar site) to assess potential NH3 impacts from local poultry installations.
- Park managed by Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Measurements collected with UKCEH ALPHA passive samplers placed on shelters at ~1.5 m height, with monthly exposure cycles.
- Data intended to support understanding of ammonia concentrations in a sensitive peatland ecosystem and inform management decisions.

## Methods and Data Collection
- Passive sampling: CEH ALPHA samplers use a citric acid–coated filter and a PTFE membrane; replicas used for reliability.
- Deployment: Replicate samplers mounted on a shelter at ~1.5 m above ground; exposed monthly.
- Analysis workflow: Exposed samplers extracted into deionised water; analyzed with SEAL AA3 colorimetric method to determine ammonia concentration.
- Calculation: Air concentration derived using known uptake rate of 0.0038422 m3 h-1 and exposure duration.
- Units: Ammonia concentration expressed as micrograms of NH3 per cubic meter of air (µg NH3 m-3).
- Data quality controls:
  - CV rule: if replicate CV > 15%, replicates/records evaluated; final valid data flagged as 103.
  - Missing samplers: assigned -9999.00 and marked invalid (-1).
  - Duration anomalies: samplers left on for longer/shorter than normal cycle flagged.
  - Local contamination or deviations: notes used to discard non-representative results; reported as averages from remaining data.
- Raw data quality concerns: some samples were exposed incorrectly or lost to weather; such data are flagged or excluded from site estimates (details in accompanying documentation).

## Dataset Content and Structure
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv containing accepted data values with appropriate flags.
- Granularity: Each row corresponds to one month of data for a single site.
- Key columns (highlights):
  - Site name, unique site identifier, network_id (BE)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Measurement (ammonia concentration, µg NH3 m-3)
  - Less than flag (indicates values below detection limit of 0.03)
  - Verification id, unit id (24 = µg NH3 m-3), Data capture (%), Validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status and flag indicators for QA/QC)
  - Month (exposure month)
- Data status and flags:
  - EMEP data flags and corresponding explanations cover data capture, validity, and reasoning (e.g., contamination, sampling period variations, detection limits, CV issues).
  - The dataset leverages EMEP flag conventions to document quality concerns and representativeness.

## Site Information and Spatial Context
- Ballynahone bog_1 to bog_8: eight sampling sites forming a transect.
- For each site:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Latitude and longitude coordinates (exact values provided per site)
  - Height of air inlet above ground: 1.5 m
- Spatial identifiers and coordinates enable GIS joins with other spatial datasets and mapping of ammonia concentrations across the transect.

## Application and GIS Considerations
- Suitable for map-based visualization of monthly NH3 concentrations across the Ballynahone Bog transect.
- Use spatial coordinates and site IDs to integrate with land-use, meteorology, and pollution source layers.
- Data quality flags should be consulted to filter or annotate results in maps and analyses (e.g., CV issues, contamination flags, missing samplers).
- The monthly granularity supports temporal trend analysis and exposure assessment across the transect.