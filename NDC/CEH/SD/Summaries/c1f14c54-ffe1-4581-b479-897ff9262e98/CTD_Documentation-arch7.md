# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- License: Open Government Licence
- Access: https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- Citation (reuse): Rovelli, L.; Attard, K. M.; Stahl, H.; Glud, R. N. (2016). In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/c1f14c54-ffe1-4581-b479897ff9262e

## Overview
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, focusing on lateral exchange in the seaward flux of C, N, and P.
- Four field campaigns measured in situ physical parameters (temperature and dissolved oxygen) in rivers with varying land–river connectivity in the Hampshire Avon catchment.
- Measurements made with CTD loggers positioned ~10 cm above the streambed; sampling frequencies ranged from 10 seconds to 5 minutes depending on site, logger unit, and battery.
- Instrument specifics:
  - Seabird SBE19: 10 s/30 s sampling; temperature resolution 0.0001°C; accuracy ±0.005°C
  - RBR XR420: 1 min sampling; temperature resolution 0.00005°C; accuracy ±0.002°C
  - Aanderaa Seaguard RCM: 5 min sampling; temperature resolution 0.001°C; accuracy ±0.03°C
- Measured parameters include near-streambed photosynthetically available radiation (PAR), water column temperature, dissolved oxygen (DO), and oxygen saturation (O2sat).

## Data structure
- Key columns: DateTime (MM/DD/YYYY hh:mm:ss), Date (MM/DD/YYYY), Time (hh:mm:ss), Temperature (°C), PAR (µmol quanta/m2/s), O2sat (%), DO (µmol/L)
- NaN values indicate data not collected (e.g., instrument cleaning, battery changes, or data download gaps) or data flagged as contaminated (fouling/debris)
- Data quality and resolution are instrument-dependent (CTD logger specifics apply)

## File naming and Sites
- Data are organized into twenty-three CSV files named CTD_SiteCode_Season.csv, covering combinations of site and season:
  - Examples: CTD_AP_autumn.csv, CTD_AP_spring.csv, CTD_AP_summer.csv, CTD_AP_winter.csv, CTD_AS_autumn.csv, CTD_AS_spring.csv, CTD_AS_summer.csv, CTD_AS_winter.csv, CTD_CE1_autumn.csv, CTD_CE1_spring.csv, CTD_CE1_summer.csv, CTD_CW2_autumn.csv, CTD_CW2_spring.csv, CTD_CW2_summer.csv, CTD_CW2_winter.csv, CTD_GA2_autumn.csv, CTD_GA2_spring.csv, CTD_GA2_summer.csv, CTD_GA2_winter.csv, CTD_GN1_autumn.csv, CTD_GN1_spring.csv, CTD_GN1_summer.csv, CTD_GN1_winter.csv
- Site codes and locations:
  - CE1: River Ebble (Latitude 51.027499, Longitude -1.9217089)
  - GA2: River Avon (Latitude 51.318289, Longitude -1.8600020)
  - GN1: River Nadder (Latitude 51.043849, Longitude -2.1118158)
  - CW2: River Wylye (Latitude 51.142475, Longitude -2.2033140)
  - AS1 (aka AP): A tributary of the River Sem (Latitude 51.055413, Longitude -2.1568407)
  - AS2 (aka AS): River Sem (Latitude 51.045826, Longitude -2.1104425)

## Field campaigns and temporal coverage
- Spring 2013: 23/04 – 09/05/2013
- Summer 2013: 31/07 – 16/08/2013
- Autumn 2013: 29/10 – 11/11/2013
- Winter 2014: 28/01 – 09/02/2014
- Note: Data collection at CE1 was not performed in winter 2014 due to flooding

## Data quality, limitations and considerations for GIS use
- Gaps and gaps-filled-like conditions represented by NaN values (e.g., instrument maintenance, data download issues, fouling)
- Data may require QA/QC, cleaning, and alignment across sites and seasons for GIS analyses
- Spatial context includes six tributaries with precise coordinates, enabling integration with catchment, land-use, or hydrographic datasets
- The dataset provides time-series measurements suitable for mapping temporal changes in light regime, DO, DO saturation, and temperature across sites and seasons

## Potential GIS applications
- Map-based visualization of near-streambed light, DO, DO saturation, and temperature across multiple tributaries and seasons
- Spatial-temporal analyses in catchment modeling, supporting interpretation of lateral exchange processes
- Integration with environmental layers (land cover, hydrology, water quality) to assess spatial patterns and drivers
- QA-ready data structuring via consistent site codes and season-based CSVs for reproducible GIS workflows