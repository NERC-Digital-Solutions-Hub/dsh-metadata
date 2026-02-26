# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

## Overview
- Location: Ballynahone National Park, Northern Ireland (ASSI/SAC and Ramsar site); ammonia-sensitive peatland.
- Purpose: assess NH3 concentrations along a transect to understand potential impacts from local poultry installations.
- Timeframe: 2014–2017, with monthly sampler exposures.
- Stakeholders: Ulster Wildlife Trust (site operator) and Centre for Ecology and Hydrology Edinburgh (analysis).

## Sampling and Analysis
- Method: CEH ALPHA® passive samplers using a citric acid coated filter and a PTFE membrane (membrane facing downwards).
- Deployment: replicates mounted on shelter poles at about 1.5 m above ground.
- Sampling frequency: monthly exposure cycles starting at the beginning of each month.
- Analysis: exposed samplers eluted in deionised water and analyzed by AMFIA (conductivity-based NH3 measurement).
- Concentration calculation: convert to average air concentration using uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Output: final dataset named UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv; a concentration value in µg NH3 m-3 per monthly period; includes data quality flags.

## Data Quality and Flagging
- Data quality controls applied to raw data:
  - Coefficient of variation (replicates) threshold: CV < 15% required for validity; if CV > 15%, replicates evaluated and may be discarded; valid data flagged as 103 when representative.
  - Missing samplers: flagged as -9999.00 and invalid (-1).
  - Sampling duration: durations longer or shorter than the normal monthly cycle are flagged.
  - Local contamination or influences: notes reviewed; questionable samplers discarded; final value is average of remaining replicates.
- Data flags and codes: accompanying EMEP/UK-AIR data status flags describe data capture, validity, detection limits, and contamination or local influences.
- Documentation: comprehensive notes on site records (e.g., local sources of contamination) and decisions to discard or accept data.

## Dataset Structure and Contents
- Format: one row per month per site.
- Key fields include:
  - Site name and unique site identifier
  - Network_id (UWT) and parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure period)
  - Measured ammonia concentration (µg NH3 m-3)
  - Less than detection flag, verification id, unit id
  - Data capture (%) and validity_id
  - EMEP data status code
  - Month-Year (mm-yy)
- Purpose: deliver a ready-to-use, GIS-friendly tabular dataset with associated quality metadata.

## Site Information
- Sampling locations: Ballynahone bog_1 to Ballynahone bog_8
- Common temporal coverage: start_date 01/09/2014; end_date ongoing at time of dataset
- Spatial attributes: latitude and longitude provided for each site; height of air inlet above ground is 1.5 m
- Data provenance: operator Ulster Wildlife Trust; analysis by Centre for Ecology and Hydrology Edinburgh

## GIS-Relevance and Use
- Suitable for map-based visualization of spatial NH3 concentrations along the transect.
- Provides precise site coordinates and temporal monthly NH3 concentration data with quality flags.
- Facilitates assessment of spatial patterns, trends, and potential contamination or data quality issues across the sampling network.