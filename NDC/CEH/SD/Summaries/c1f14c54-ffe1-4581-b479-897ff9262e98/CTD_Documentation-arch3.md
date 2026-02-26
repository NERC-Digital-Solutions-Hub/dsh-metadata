# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Access and reuse
- Data licensed under the Open Government Licence; accessible at https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- Reuse requires citation: Rovelli, L.; Attard, K. M.; Stahl, H.; Glud, R. N. (2016). In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/c1f14c54-ffe1-4581-b479897ff9262e

## Overview
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer (Queen Mary University of London), studying lateral exchange in C, N, and P flux.
- Four field campaigns measuring in situ physical parameters (temperature and dissolved oxygen) in rivers with varying land-river connectivity within the Hampshire Avon catchment.
- Measurements collected with CTD loggers positioned about 10 cm above the streambed; sampling intervals ranged from 10 seconds to 5 minutes, depending on site, instrument, and battery life.
- Instruments used include Seabird SBE19 (temperature ~0.0001°C resolution; 0.005°C accuracy), RBR XR420 (0.00005°C resolution; ±0.002°C), and Aanderaa Seaguard RCM (5 min intervals; 0.001°C resolution; ±0.03°C).
- Data structured to capture near-streambed conditions such as temperature, dissolved oxygen, dissolved oxygen saturation, and photosynthetically available radiation (PAR).

## File naming and site codes
- Data are organized into 23 CSV files named CTD_<SiteCode>_<Season>.csv
  - Examples: CTD_AP_autumn.csv, CTD_AP_spring.csv, CTD_AP_summer.csv, CTD_AP_winter.csv, CTD_AS_autumn.csv, CTD_AS_spring.csv, CTD_AS_summer.csv, CTD_AS_winter.csv, CTD_CE1_autumn.csv, CTD_CE1_spring.csv, CTD_CE1_summer.csv, CTD_CW2_autumn.csv, CTD_CW2_spring.csv, CTD_CW2_summer.csv, CTD_CW2_winter.csv, CTD_GA2_autumn.csv, CTD_GA2_spring.csv, CTD_GA2_summer.csv, CTD_GA2_winter.csv, CTD_GN1_autumn.csv, CTD_GN1_spring.csv, CTD_GN1_summer.csv, CTD_GN1_winter.csv
- Site codes and locations:
  - CE1: River Ebble (51.027499, -1.9217089)
  - GA2: River Avon (51.318289, -1.8600020)
  - GN1: River Nadder (51.043849, -2.1118158)
  - CW2: River Wylye (51.142475, -2.2033140)
  - AS1 (aka AP): tributary of River Sem (51.055413, -2.1568407)
  - AS2 (aka AS): River Sem (51.045826, -2.1104425)

## Field campaigns and coverage
- Campaigns conducted in Spring 2013 (23/04–09/05/2013), Summer 2013 (31/07–16/08/2013), Autumn 2013 (29/10–11/11/2013), and Winter 2014 (28/01–09/02/2014).
- Data collection at site CE1 not performed in winter 2014 due to flooding.

## Data structure and quality notes
- NaN values indicate data not collected (e.g., instrument maintenance, battery changes, data download issues) or data flagged as contaminated (e.g., fouling or debris).
- Columns include:
  - DateTime, Date, Time: timestamps with formats (MM/DD/YYYY hh:mm:ss, etc.)
  - Temperature: water column temperature in °C; instrument-specific resolution/accuracy
  - PAR: near-streambed photosynthetically available radiation, in µmol quanta/m²/s (±3% accuracy)
  - O2sat: oxygen saturation as a percentage (%), relative to atmospheric equilibrium; resolution ~0.4%, accuracy ~1.5%
  - DO: dissolved oxygen concentration in µmol/L; resolution <1 µmol/L, accuracy ~8 µmol/L (or 5%)
- Data come from multiple instrument types, with respective performance characteristics and potential site-specific variations.

## Relevance for monitoring framework authors
- Demonstrates open data practices with clear licensing, citation requirements, and direct linkage to a data centre.
- Provides a multi-site, seasonally resolved dataset with explicit metadata on instrument types, sampling frequencies, and data gaps, useful for evaluating data quality, interoperability, and governance considerations in monitoring programs.
- Highlights practical challenges relevant to monitoring frameworks:
  - Handling data gaps (NaNs) and ensuring traceability of when data were not collected or contaminated
  - Managing metadata completeness across instruments and sites
  - Integrating data from different sensors with varying resolutions and accuracies
  - Ensuring data accessibility and appropriate data sharing while preserving provenance and citation requirements