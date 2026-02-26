# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- Data licensed under Open Government Licence.
- Accessible via https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e.
- If reused, must cite: Rovelli, L.; Attard, K. M.; Stahl, H.; Glud, R. N. (2016). In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/c1f14c54-ffe1-4581-b479897ff9262e.

## Overview
- Dataset from the stream metabolism component of the NERC Macronutrients consortium (led by Prof. Mark Trimmer, QMUL) examining lateral exchange in C, N, and P flux.
- Data collected in four field campaigns measuring in situ physical parameters (temperature and dissolved oxygen) across rivers with varying land-river connectivity in the Hampshire Avon catchment.
- Instruments and placement:
  - CTD loggers positioned about 10 cm above the streambed.
  - Seabird SBE19: 10 s to 30 s sampling intervals; temperature resolution 0.0001 °C; accuracy ±0.005 °C.
  - RBR XR420: 1 min intervals; temperature resolution 0.00005 °C; accuracy ±0.002 °C.
  - Aanderaa Seaguard RCM: 5 min intervals; temperature resolution 0.001 °C; accuracy ±0.03 °C.

## Data structure and file naming
- 23 data files named by riverine site and season: CTD_<SiteCode>_<Season>.csv
  - Examples: CTD_AP_autumn.csv, CTD_AP_spring.csv, CTD_AP_summer.csv, CTD_AP_winter.csv, CTD_AS_autumn.csv, CTD_AS_spring.csv, CTD_AS_summer.csv, CTD_AS_winter.csv, CTD_CE1_autumn.csv, CTD_CE1_spring.csv, CTD_CE1_summer.csv, CTD_CW2_autumn.csv, CTD_CW2_spring.csv, CTD_CW2_summer.csv, CTD_CW2_winter.csv, CTD_GA2_autumn.csv, CTD_GA2_spring.csv, CTD_GA2_summer.csv, CTD_GA2_winter.csv, CTD_GN1_autumn.csv, CTD_GN1_spring.csv, CTD_GN1_summer.csv, CTD_GN1_winter.csv.
- SiteCodes and locations:
  - CE1: River Ebble (Latitude 51.027499, Longitude -1.9217089)
  - GA2: River Avon (Latitude 51.318289, Longitude -1.8600020)
  - GN1: River Nadder (Latitude 51.043849, Longitude -2.1118158)
  - CW2: River Wylye (Latitude 51.142475, Longitude -2.2033140)
  - AS1 (AP): Tributary of River Sem (Latitude 51.055413, Longitude -2.1568407)
  - AS2 (AS): River Sem (Latitude 51.045826, Longitude -2.1104425)
- Seasons represented: spring, summer, autumn, winter (field campaigns 2013 and 2014).

## Field campaigns and coverage
- Spring 2013: 23/04 – 09/05/2013
- Summer 2013: 31/07 – 16/08/2013
- Autumn 2013: 29/10 – 11/11/2013
- Winter 2014: 28/01 – 09/02/2014
- Note: Data collection at site CE1 not performed in winter 2014 due to flooding.

## Data columns and quality notes
- Core fields:
  - DateTime: combined date and time (format MM/DD/YYYY hh:mm:ss)
  - Date: date string (MM/DD/YYYY)
  - Time: time string (hh:mm:ss)
  - Temperature: water column temperature [°C]
  - PAR: photosynthetically available radiation near streambed [µmol quanta/m²/s] (±3% accuracy)
  - O2sat: dissolved oxygen saturation relative to atmospheric equilibrium [%] (resolution ~0.4%, accuracy ~1.5%)
  - DO: dissolved oxygen concentration [µmol/L] (resolution <1 µmol/L, accuracy ~8 µmol/L or 5%)
- Data quality indicators:
  - NaN values indicate not collected (e.g., instrument cleaning, battery change, data download) or contaminated readings (fouling/debris).
  - Instrument-specific performance details provided (resolution/accuracy per device).
- Data are provided as a structured, multi-file dataset enabling site- and season-specific exploration.

## Licensing and provenance
- Data originate from the NERC Macronutrients project and field campaigns led by collaborating institutions.
- Clear provenance: field collection by named researchers; compilation into 23 site-season files; linked to the overarching dataset on the NERC Environmental Information Data Centre.
- Users should cite Rovelli et al. (2016) when reusing the data, per the provided citation.