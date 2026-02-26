# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- Data are released under the Open Government Licence.
- Access via DOI: https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- Reuse requires citation: Rovelli et al. (2016), NERC Environmental Information Data Centre dataset.

## Overview
- Compiled from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer (QMUL).
- Four field campaigns measuring in situ physical parameters (temperature, dissolved oxygen) in rivers with varying land–river connectivity within the Hampshire Avon catchment.
- Measurements collected with CTD loggers positioned ~10 cm above the streambed.
- Instruments and sampling:
  - Seabird SBE19: ~10 s intervals, temperature resolution 0.0001°C, accuracy ±0.005°C.
  - RBR XR420: ~1 min intervals, temperature resolution 0.00005°C, accuracy ±0.002°C.
  - Aanderaa Seaguard RCM: ~5 min intervals.
  - PAR (photosynthetically active radiation) readings: accuracy ±3%.
  - Dissolved oxygen saturation (O2sat) and dissolved oxygen (DO) concentrations with specified resolutions and accuracies.

## Data collection and structure
- Field campaigns: Spring 2013 (23/04–09/05/2013), Summer 2013 (31/07–16/08/2013), Autumn 2013 (29/10–11/11/2013), Winter 2014 (28/01–09/02/2014).
- Not collected at site CE1 in winter due to flooding.
- Data files: 23 CSV files named CTD_SiteCode_Season.csv (e.g., CTD_AP_autumn.csv, CTD_GN1_winter.csv), each representing a site-season dataset.
- SiteCodes and locations:
  - CE1 – River Ebble
  - GA2 – River Avon
  - GN1 – River Nadder
  - CW2 – River Wylye
  - AS1 (aka AP) – tributary of River Sem
  - AS2 (aka AS) – River Sem
  - Coordinates provided for each site
- Data columns and units:
  - DateTime, Date, Time formats specified
  - Temperature (°C) in water column
  - PAR (µmol quanta/m2/s) with ~3% accuracy
  - O2sat (%) – percentage saturation (resolution ~0.4%, accuracy ~1.5%)
  - DO (µmol/L) – dissolved oxygen concentration (resolution <1 µmol/L, accuracy ~8 µmol/L or 5%)
  - NaN is used for data not collected (e.g., instrument downtime, cleaning, fouling) or contaminated readings

## Data quality, gaps, and notes
- Data gaps and irregular sampling due to field conditions and sensor maintenance (e.g., battery changes, cleaning, data downloads).
- Some measurements flagged as contaminated or not collected, explicitly represented as NaN.
- Cross-site comparisons should account for differing sampling frequencies, instrument types, and environmental conditions.

## Authors, project, and provenance
- Field and data collection led by L. Rovelli, K. M. Attard, H. Stahl; supervision by R. N. Glud.
- Part of the NERC Macronutrients consortium’s study on lateral exchange in carbon, nitrogen, and phosphorus flux.
- Data stewardship aligned with open data practices and structured for discoverability via multiple site-season CSV files.

## Practical implications for data strategy
- Open licensing with clear citation fosters reuse and integration into broader analyses.
- Well-structured file naming and comprehensive metadata (instrument specs, sampling intervals, site coordinates) support discoverability and interoperability.
- Transparency about data gaps and measurement limitations aids accurate modeling and uncertainty assessment.
- Metadata decisions enable future updates and potential supplementation with additional campaigns or related datasets.