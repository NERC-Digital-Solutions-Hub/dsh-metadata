# In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014

## Purpose and scope
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium led by Prof. Mark Trimmer, focusing on near-streambed light regime, dissolved oxygen (DO) dynamics, and temperature across six tributaries of the Hampshire Avon catchment.
- Four field campaigns conducted to measure in situ physical parameters in rivers with varying land–river connectivity.
- Data collected to support understanding of lateral exchange and fluxes of C, N, and P.

## Data collection and methods
- Field campaigns: spring 2013 (23/04–09/05/2013), summer 2013 (31/07–16/08/2013), autumn 2013 (29/10–11/11/2013), winter 2014 (28/01–09/02/2014). Data collection not performed at CE1 in winter due to flooding.
- Instrumentation: CTD loggers positioned about 10 cm above the streambed.
  - Seabird SBE19: sampling ~10–30 s, temperature resolution 0.0001°C, accuracy ±0.005°C.
  - RBR XR420: sampling ~1 min, temperature resolution 0.00005°C, accuracy ±0.002°C.
  - Aanderaa Seaguard RCM: sampling ~5 min, temperature resolution 0.001°C, accuracy ±0.03°C.
- Measured parameters: water temperature, near-streambed PAR (photosynthetically available radiation), DO (micromoles per liter), and DO saturation (%). PAR accuracy ±3%.

## Site codes and data structure
- Six river tributaries and codes:
  - CE1: River Ebble
  - GA2: River Avon
  - GN1: River Nadder
  - CW2: River Wylye
  - AS1 (aka AP): tributary of the River Sem
  - AS2 (aka AS): River Sem
- Data organization:
  - 23 separate CSV files named CTD_<SiteCode>_<Season>.csv (season: autumn, spring, summer, winter).
  - Site coordinates provided (latitude/longitude) for location reference.
- Data columns and units:
  - DateTime, Date, Time
  - Temperature (°C)
  - PAR (µmol quanta/m2/s), PAR accuracy ±3%
  - O2sat (% saturation)
  - DO (µmol/L)
  - Data gaps or flagged data indicated by NaN (e.g., during instrument maintenance, fouling, or data download issues)

## Data quality and limitations
- Data gaps due to practical field challenges (battery changes, cleaning, data downloads) and environmental conditions.
- Some data not collected at specific sites during certain campaigns (e.g., CE1 winter due to flooding).
- Instrument-specific accuracy and resolution documented to inform QA and interpretation.

## Access and reuse
- Data available under the Open Government Licence.
- DOI: https://doi.org/10.5285/c1f14c54-ffe1-4581-b479-897ff9262e
- Suggested citation: Rovelli, L.; Attard, K. M.; Stahl, H.; Glud, R. N. (2016). In situ near-streambed light regime and water column dissolved oxygen and temperature measurements performed seasonally at six tributaries of Hampshire River Avon from 2013 to 2014. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/c1f14c54-ffe1-4581-b479897ff9262e

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, QA-friendly dataset of near-bed light, DO, and temperature across multiple tributaries and seasons, suitable for time-series analyses and cross-site comparisons.
- Can be integrated with other environmental datasets to evaluate lateral exchange processes and nutrient/carbon fluxes in the Hampshire River Avon catchment.
- Supports the broader aim of demonstrating environmental health and policy performance over time through consistent data formatting and accessible metadata.