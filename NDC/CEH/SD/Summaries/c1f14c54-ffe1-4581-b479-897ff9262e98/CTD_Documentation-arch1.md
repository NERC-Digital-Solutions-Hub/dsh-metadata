# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- Data are available under the Open Government Licence.
- Accessible at the provided DOI: https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- When reused, dataset citation is required: Rovelli et al. (2016), NERC Environmental Information Data Centre.

## Overview
- Compiled from the stream metabolism component of the NERC Macronutrients consortium (led by Prof. Mark Trimmer, QMUL) focusing on lateral exchange in the seaward flux of C, N and P.
- Four field campaigns measured in situ physical parameters (temperature, dissolved oxygen) across rivers with varying land-river connectivity in the Hampshire Avon catchment.
- Measurements made with CTD loggers positioned ~10 cm above the streambed.
- Instrument details and sampling cadence:
  - Seabird SBE19: 10 s and 30 s intervals; temperature resolution 0.0001 °C; accuracy ±0.005 °C.
  - RBR XR420: 1 min intervals; temperature resolution 0.00005 °C; accuracy ±0.002 °C.
  - Aanderaa Seaguard RCM: 5 min intervals; temperature resolution 0.001 °C; accuracy ±0.03 °C.
- Data include near-streambed photosynthetically available radiation (PAR) and water-column dissolved oxygen (DO) measurements.

## Data structure
- Columns include:
  - DateTime, Date, Time
  - Temperature (°C) in the water column
  - PAR (µmol quanta/m2/s) near the streambed
  - O2sat (%) dissolved oxygen saturation relative to atmospheric equilibrium
  - DO (µmol/L) dissolved oxygen concentration
- Instrument data resolution and accuracy depend on the specific logger used.
- NaN values indicate data not collected (e.g., instrument cleaning, battery issues, data download gaps) or data contaminated (fouling/debris).

## File naming
- 23 CSV data files named CTD_SiteCode_Season.csv, e.g.:
  - CTD_AP_autumn.csv, CTD_AP_spring.csv, CTD_AP_summer.csv, CTD_AP_winter.csv
  - CTD_AS_autumn.csv, CTD_AS_spring.csv, CTD_AS_summer.csv, CTD_AS_winter.csv
  - CTD_CE1_autumn.csv, CTD_CE1_spring.csv, CTD_CE1_summer.csv
  - CTD_CW2_autumn.csv, CTD_CW2_spring.csv, CTD_CW2_summer.csv, CTD_CW2_winter.csv
  - CTD_GA2_autumn.csv, CTD_GA2_spring.csv, CTD_GA2_summer.csv, CTD_GA2_winter.csv
  - CTD_GN1_autumn.csv, CTD_GN1_spring.csv, CTD_GN1_summer.csv, CTD_GN1_winter.csv

## SiteCodes
- CE1: River Ebble (Latitude 51.027499, Longitude -1.9217089)
- GA2: River Avon (Latitude 51.318289, Longitude -1.8600020)
- GN1: River Nadder (Latitude 51.043849, Longitude -2.1118158)
- CW2: River Wylye (Latitude 51.142475, Longitude -2.2033140)
- AS1 (aka AP): A tributary of the River Sem (Latitude 51.055413, Longitude -2.1568407)
- AS2 (aka AS): River Sem (Latitude 51.045826, Longitude -2.1104425)

## Field campaigns
- Spring 2013: 23/04 – 09/05/2013
- Summer 2013: 31/07 – 16/08/2013
- Autumn 2013: 29/10 – 11/11/2013
- Winter 2014: 28/01 – 09/02/2014
- Note: Data collection was not performed at site CE1 in winter 2014 due to flooding.