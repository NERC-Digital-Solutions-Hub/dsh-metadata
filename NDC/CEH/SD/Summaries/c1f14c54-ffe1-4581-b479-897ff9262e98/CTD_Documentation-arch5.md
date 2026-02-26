# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- Data available under the Open Government Licence.
- Access: https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- Reuse requires citation: Rovelli, L.; Attard, K. M.; Stahl, H.; Glud, R. N. (2016). In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/c1f14c54-ffe1-4581-b479897ff9262e

## Overview
- Dataset from the stream metabolism component of the NERC Macronutrients consortium led by Prof. Mark Trimmer (Queen Mary University of London) titled “The role of lateral exchange in the seaward flux of C, N and P.”
- Field campaigns measured in situ physical parameters (temperature and dissolved oxygen) in rivers within the Hampshire Avon catchment.
- Data collected using CTD loggers positioned ~10 cm above the streambed; campaigns spanned varying land-river connectivity.
- Instruments and performance: Seabird SBE19 (temperature measurements at 10–30 s intervals; temp resolution 0.0001°C, accuracy ±0.005°C); RBR XR420 (1 min intervals; temperature resolution 0.00005°C, accuracy ±0.002°C); Aanderaa Seaguard RCM (5 min intervals; temperature resolution 0.001°C, accuracy ±0.03°C).
- Data collection led by Dr. L. Rovelli, Dr. K. Attard, Assoc. Prof. H. Stahl, under Prof. R.N. Glud.

## Field campaigns and sites
- Field campaigns: Spring 2013 (23/04–09/05/2013); Summer 2013 (31/07–16/08/2013); Autumn 2013 (29/10–11/11/2013); Winter 2014 (28/01–09/02/2014).
- Data collection not performed at site CE1 in winter due to flooding.
- Sites and site codes (with approximate locations):
  - CE1 (River Ebble): 51.027499 N, -1.9217089 W
  - GA2 (River Avon): 51.318289 N, -1.8600020 W
  - GN1 (River Nadder): 51.043849 N, -2.1118158 W
  - CW2 (River Wylye): 51.142475 N, -2.2033140 W
  - AS1 (aka AP) (tributary of River Sem): 51.055413 N, -2.1568407 W
  - AS2 (aka AS) (River Sem): 51.045826 N, -2.1104425 W

## Data structure and variables
- Data files are organized as 23 separate CSV files named CTD_SiteCode_Season.csv.
  - Examples: CTD_AP_autumn.csv, CTD_AP_spring.csv, CTD_AP_summer.csv, CTD_AP_winter.csv, CTD_AS_autumn.csv, CTD_AS_spring.csv, CTD_AS_summer.csv, CTD_AS_winter.csv, CTD_CE1_autumn.csv, CTD_CE1_spring.csv, CTD_CE1_summer.csv, CTD_CW2_autumn.csv, CTD_CW2_spring.csv, CTD_CW2_summer.csv, CTD_CW2_winter.csv, CTD_GA2_autumn.csv, CTD_GA2_spring.csv, CTD_GA2_summer.csv, CTD_GA2_winter.csv, CTD_GN1_autumn.csv, CTD_GN1_spring.csv, CTD_GN1_summer.csv, CTD_GN1_winter.csv.
- SiteCodes and coordinates are provided to map data to locations.
- Data columns (example structure):
  - DateTime: timestamp (MM/DD/YYYY hh:mm:ss)
  - Date: date (MM/DD/YYYY)
  - Time: time (hh:mm:ss)
  - Temperature: water temperature in °C (instrument-dependent resolution/accuracy)
  - PAR: near-streambed photosynthetically available radiation (µmol quanta/m2/s), accuracy ±3%
  - O2sat: dissolved oxygen saturation (% of atmospheric equilibrium), resolution 0.4%, accuracy 1.5%
  - DO: dissolved oxygen concentration (µmol/L), resolution <1 µmol/L, accuracy 8 µmol/L (or 5%)

## Data quality, completeness, and limitations
- NaN entries indicate data not collected (e.g., instrument cleaning, battery changes, data download) or data flagged as contaminated (fouling/debris).
- Temperature, PAR, O2sat, and DO data are instrument-specific with stated resolutions and accuracies.
- Seasonal and site-level coverage varies; CE1 had winter data missing due to flooding, affecting cross-season comparability for that site.

## Licensing, provenance, and governance
- Clear licensing and citation requirements to ensure proper reuse.
- Data provenance documented through field campaigns, instruments, sampling regimes, and site metadata.
- File naming and site coding provide traceability and facilitate data discovery and interoperability across large datasets.

## Practical considerations for reuse and governance
- Ensure proper citation per the dataset’s specified format.
- Verify instrument-specific units and resolutions per file when aggregating data across sites.
- Be aware of potential data gaps or quality flags (NaNs) when analyzing seasonal comparisons or meta-analyses.
- Use the provided site coordinates for spatial analyses and reproducibility.