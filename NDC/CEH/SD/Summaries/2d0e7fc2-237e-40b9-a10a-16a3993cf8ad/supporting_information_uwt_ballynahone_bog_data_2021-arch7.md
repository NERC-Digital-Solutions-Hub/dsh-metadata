# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Overview
- Study area: Ballynahone National Park in Northern Ireland, an Area of Special Scientific Interest (ASSI/SAC) and Ramsar site.
- Purpose: Assess potential ammonia (NH3) impacts on a sensitive peatland ecosystem due to local poultry livestock installations.
- Operators and analysts: Ballynahone Bog field site operated by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Data collection: UKCEH ALPHA passive samplers deployed along a transect through the bog; samplers exposed monthly.
- Output: Concentrations reported as average NH3 in air (µg NH3 m-3) for each site and exposure period.

## Methods (UKCEH ALPHA sampler)
- Sampler design: Passive samplers with citric acid coated filter and a protective PTFE membrane; exposed with membrane end facing downward at ~1.5 m height.
- Replication: Multiple samplers per site to improve reliability.
- Analysis workflow: Exposed samplers are eluted into deionised water; NH3 quantified by SEAL AA3 colorimetric analysis; results converted to average air concentration using a known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data capture: Raw data include some improperly exposed or weather-affected samples; such data are flagged and excluded from deposition estimates.
- Data quality assessment: Data quality rules include:
  - CV of replicates < 15% for valid results; otherwise evaluated and possibly discarded.
  - Missing samplers flagged (-9999.00; invalid -1).
  - Variations in sampler duration (long/short) due to weather or staffing.
  - Local contamination or influences noted by site operators; non-representative results discarded if appropriate.
- Final dataset: UWT_Ballynahone_Bog_Data_2021.csv containing accepted data with appropriate flags; includes site names and spatial identifiers.

## Data structure and contents
- Dataset: UWT_Ballynahone_Bog_Data_2021.csv
- Core columns (per monthly record for a single site):
  - Site name and unique site identifier
  - Network_id (BE)
  - Parameter_id (e.g., alpha_NH3_g)
  - Measurement start date and start time; measurement end date and end time
  - Ammonia concentration (µg NH3 m-3) for the exposure period
  - Less than detection limit flag (0/1)
  - Verification id (Not verified / Preliminary verified / Verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP data status code and related flags
  - Month-Year of measurement (MMM-YY)
- Notes: Final values reflect the average concentration for each monthly exposure period after applying quality controls and excluding non-representative or invalid samples.

## Site information and location
- Ballynahone bog_1 to bog_8 (eight sampling sites)
- Start date for all sites: 01/09/2014; End date: Ongoing
- Coordinates (approximate, WGS84):
  - bog_1: lat 54.82223827, lon -6.67860685
  - bog_2: lat 54.82303694, lon -6.67686906
  - bog_3: lat 54.82331637, lon -6.67530382
  - bog_4: lat 54.82396942, lon -6.67339952
  - bog_5: lat 54.82446239, lon -6.67000651
  - bog_6: lat 54.82514962, lon -6.67946104
  - bog_7: lat 54.82165647, lon -6.67468906
  - bog_8: lat 54.8161610, lon -6.6559670
- Inlet height above ground: 1.5 m for all sites
- Context: Sites form a transect within Ballynahone Bog, aligning with the broader park/ASSI/SAC/Ramsar designations.

## GIS and data-use considerations
- Suitability for map-based visualization:
  - Spatially explicit NH3 concentration data across eight transect sites enables choropleth or point maps over time.
  - Replicate data and quality flags allow users to filter for high-confidence measurements.
- Data quality and standards:
  - Apply CV, duration, and contamination flags to determine which records are suitable for analysis and visualization.
  - EMEP status codes and verification levels provide context for cross-reference with national/international datasets.
- Integration opportunities:
  - Combine with other emissions, meteorology, or land-use layers to model spatial patterns and exposures.
  - Align with GIS workflows to create time-enabled maps showing monthly NH3 concentrations along the transect.
- Limitations and gaps:
  - Some data excluded due to weather, sampling errors, or contamination; remaining records may have varying data capture percentages.
  - Resolution is site-level along a transect; finer-scale spatial inference may require additional data or models.
  - Dataset uses coordinates in decimal degrees; ensure consistent CRS (WGS84) when integrating with other GIS layers.