# Soil respiration under Miscanthus x giganteus and an adjacent barley crop

## Overview
- Comparative field study of soil respiration (Rs) under Miscanthus x giganteus vs adjacent barley.
- Measurements taken May–August 2013 on a farm in eastern United Kingdom.
- Utilised automated chambers with infrared gas analysers (IRGA) to quantify Rs.

## Study site and experimental design
- Location: East UK farm; fields with a seven-year-old Miscanthus stand and an April-sown spring barley crop in adjacent plots.
- Instrumentation: One IRGA (Licor LI-8100-101A) and one multiplexer per crop.
- Replication: Six chambers per crop, placed randomly within separate plots (≥1.5 m apart) and treated as independent replicates.
- Chamber setup: PVC collars (diameter 20 cm, height 10 cm) inserted ~2 cm into soil; no above-ground vegetation included; collars did not exclude roots.
- Complementary measurements: Soil temperature and soil moisture at 5 cm depth near collars; hourly meteorological data (solar radiation, air temperature) onsite.

## Measurements and data collection
- Rs measurement process: Chambers closed for 2 minutes with a 30-second dead band; cycle repeated across chambers.
- Data captured: CO2 concentration over time to derive Rs; chamber air temperature recorded; spatial arrangement allowed comparison between crops.

## Data processing and analyses
- Rs flux calculation: Linear regression of CO2 concentration against time; corrected for chamber volume and temperature using manufacturer software.
- Statistical tools: Analyses conducted in SAS 9.3.

## Datasets included
- Dataset 1. Flux_and_soil_data
  - Key fields: DATE, CROP (ARAB = barley, MISC = Miscanthus), DTHOUR, DTQUART, TIME, Rs_Umol (µmol m^-2 s^-1), Rs_mg (mg m^-2 h^-1), Rs_r2, CHAMBERTEMP (°C), CHANNEL, Rs_cv, AREA (cm^2), ST_C (soil temp at 5 cm, °C), SM_M3M3 (volumetric soil moisture), plus additional metadata.
  - Structure: Measurements across time with hourly/15-minute granularity; includes per-chamber replication data.
- Dataset 2. Met_data
  - Key fields: Datetime, AIRTEMP_C (air temperature), RAD_WMSQ (solar radiation).
  - Structure: Meteorological context synchronized with Rs measurements.

## References and data provenance
- Primary data citation: Keane, B.; Ineson, P. (2017). Soil respiration under Miscanthus x giganteus and an adjacent barley crop. NERC Environmental Information Data Centre. DOI: https://doi.org/10.5285/c397d6f4-96f4-4967-a0df-c64ef35ea572
- Related methodological context: Drewer et al. (2012) on crop-type effects on soil gas emissions; Heinemeyer et al. (2011) on measurement and collar-depth considerations.

## Notes for analysts
- Data scope: Field-scale, replicated measurements across two crop types in a single farm setting during a defined growing season.
- Data handling: Rs derived via linear regression against time; results linked to chamber-specific conditions (temperature, area) and soil moisture.
- Access and citation: Dataset is citable and accompanied by metadata; primary data and methods are described to enable re-analysis and model development.