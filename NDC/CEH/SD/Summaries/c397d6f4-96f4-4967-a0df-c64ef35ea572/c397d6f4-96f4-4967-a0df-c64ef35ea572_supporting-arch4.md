# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

## Overview
- Dataset citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572
- Study context: measurements beneath a seven-year-old Miscanthus stand and an adjacent April-sown spring barley field on a UK farm.
- Study period: May–August 2013.
- Experimental setup: one infrared gas analyser (IRGA) and one multiplexer per crop; six chambers per field placed randomly within plots (≥1.5 m apart); PVC collars (20 cm diameter, 10 cm high) inserted ~2 cm into soil.
- Variables monitored: soil respiration (Rs); soil temperature and moisture at 5 cm depth; hourly meteorological data (solar radiation, air temperature).

## Study design and measurement setup
- Chamber system: automated chambers with IRGA; chambers closed for 2 minutes per measurement cycle with a 30-second dead band between chambers; cycles sequential across chambers.
- Replication and controls: chambers treated as independent replicates; collars not designed to exclude roots; no above-ground vegetation included in Rs measurements.
- Environmental monitoring: 5 cm depth soil temperature (ST_C) and volumetric soil moisture (SM_M3M3) recorded; onsite weather station captured solar radiation and air temperature.

## Data collection, processing and analysis
- Rs calculation: Rs fluxes computed as linear regressions of CO2 concentration versus time; corrected for chamber volume and temperature using instrument software; subsequent analyses conducted in SAS 9.3.
- Data organization: two datasets with defined metadata and units described below.

## Datasets

- Dataset 1. Flux_and_soil_data
  - Core fields:
    - DATE, DTHOUR, DTQUART, TIME
    - CROP (ARAB = barley, MISC = Miscanthus)
    - Rs_Umol (µmol m^-2 s^-1)
    - Rs_mg (mg m^-2 h^-1)
    - Rs_r2 (coefficient of determination for Rs measurement)
    - CHAMBERTEMP (°C)
    - CHANNEL (chamber number)
    - Rs_cv (coefficient of variation)
    - AREA (soil area covered by chamber, cm^2)
    - ST_C (soil temp at 5 cm, °C)
    - SM_M3M3 (volumetric soil moisture at 5 cm, m^3 m^-3)
  - Structure: Date/Time fields and quantitative measurements per observation.

- Dataset 2. Met_data
  - Core fields:
    - Datetime (dd/mm/yyyy hh:mm:ss)
    - AIRTEMP_C (air temperature, °C)
    - RAD_WMSQ (solar radiation, W m^-2)
  - Structure: Meteorological context aligned with Rs measurements.

## Data quality and provenance
- Data provenance: gathered with standardized instruments and protocols; Rs computed via manufacturer software and documented in methods.
- Metadata richness: explicit descriptions of fields, units, and sampling cadence to support discoverability, reuse, and interoperability.

## Access and references
- Related methodological and context references:
  - Drewer, J.; Finch, J. W.; Lloyd, C. R.; Baggs, E. M.; Skiba, U. (2012). How do soil emissions of N2O, CH4 and CO2 from perennial bioenergy crops differ from arable annual crops? Global Change Biology Bioenergy, 4, 408-419.
  - Heinemeyer, A.; et al. (2011). Soil respiration: implications of the plant-soil continuum and respiration chamber collar-insertion depth on measurement and modelling of soil CO2 efflux rates in three ecosystems. European Journal of Soil Science, 62, 82-94.
- Note: The dataset is published with a formal citation and DOI for proper attribution and reuse.