# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access
- Data are available from the Environmental Information Data Centre (EIDC) under the dataset: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- Access URL: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

## Data structure
- Dataset: CLM_AWS_2024_summaryQA.csv
- Contents: 1 spreadsheet with 10 columns and 367 rows
- Data quality marks: NA for unrecorded data; faulty data replaced by -9999
- Variables (approximate): Date (Year-Month-Day); Mean_air_temperature_degC; Minimum_air_temperature_degC; Maximum_air_temperature_degC; Rainfall_mm; Air_pressure_mbar; Solar_radiation_kW_per_m2; Photosynthetic active radiation (PAR) in umol m-2 s-1; Wind_speed_m_per_sec; Wind_direction_degrees

## Site overview
- Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W)
- Purpose: Climate change manipulation experiment since 1998 to simulate drought and warming over 20–30 years
- Technology: Automated roof systems powered by solar and wind
- Habitat: upland moorland dominated by Calluna vulgaris (heather)
- Treatments: replicated drought and warming plots with a set of control plots
- Soil: humo-ferric podzol with variable horizons (Eg, Bh, etc.)
- Vegetation: includes Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum and bryophytes; annual litterfall ~177 g m-2

## Climate change treatment information
- Experimental design: two treatments (drought and warming), each with three replicate plots; three control plots (total n=9 plots)
- Drought treatment: automated retractable polyethylene roof; implemented May–Sept (1999–2011); extended to Apr–Oct since 2012; reduced annual rainfall by ~20%; some rain events missed due to detection limits; in 2016–2017 adjustments due to water on roofs
- Warming treatment: retractable aluminium mesh curtains to trap infrared radiation; roofs operate at night, triggered by light level and rain detection to minimize rainfall loss; average annual rainfall reduction ~14%
- Frame maintenance: frames refurbished and new frames installed on top of old structures in June 2017 to minimize vegetation disturbance
- Data notes: sections 6(a) and 6(b) provide year-by-year drought and warming details, including growing degree days (GDD) calculations
- Data gaps and issues: rainfall sensor on site broken since Jan 2018; COVID-19 impacts and years with incomplete data; some years with missing rainfall data or laboratory measurements noted

## Equipment, protocols and data processing methodology
- On-site AWS (met station): records meteorological data; also hosts micro-met sensors within treatment plots
- Data cadence and processing:
  - AWS sensors: measurements taken every minute; hourly averages produced
  - Data quality control: manual visual checks in Excel (preferred over automated hard limits for context)
- Micro-meteorological data (plot level): daily measurements of soil and air temperature, soil moisture; soil temperature at 5, 10, 20 cm; soil moisture via TDR sensors (CS616); prior methods included manual theta probe
- Rainfall data (site level): ground-level rain gauge with 12.7 cm funnel; rainfall captured biweekly; preferred when hourly data are unavailable due to robustness against logger/power issues
- Throughfall data (plot level rainfall): plot-level rainfall collected with funnels and bottles; biweekly; data adjusted to reflect annual/seasonal rainfall by applying plot-level percent reductions to site-level rainfall; plots with incomplete data are excluded from treatment means; infilling with average reductions used in some cases
- Data availability: not all data are stored at EIDC; for additional details, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)

## AWS micro-meteorological data and sensors
- Sensors and measurements:
  - Air temperature (HMP 45C)
  - Relative humidity (0–100%)
  - Solar radiation (Skye SP1110 pyranometer)
  - PAR (SKP215 Quantum Sensor)
  - Net radiation (NR-Lites)
  - Barometric pressure (CS100)
  - Rainfall (ARG100 tipping bucket)
  - Wind speed/direction (Windsonic 2D)
- Data cadence: minute-level measurements; hourly averages; data quality checked visually in Excel
- Sensor mounting: initial height at 1 m; moved to 4 m mast after 2007 due to thefts

## Data collection and additional datasets
- Plot-level micro-met data: daily soil/air temperatures and soil moisture; sampling methods evolved (manual to TDR); post-2016 logging: half-hour averages
- Rainfall and rainfall chemistry: site-level rain gauge (biweekly); rainfall chemistry measurements; throughfall data used to derive plot-level rainfall changes
- Vegetation and chemistry data: plant biomass, canopy reflectance, phenology, vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) recorded at varying frequencies
- Appendix figures: site layout and quadrat measurements

## Summary of data usability and considerations for analysis
- Data are suitable for assessing treatment effects on climate variables, rainfall partitioning, and ecosystem responses (soil, vegetation, and carbon flux metrics)
- Users should account for:
  - Missing data associated with sensor issues and COVID-related interruptions
  - Methods used to derive plot-level rainfall from site-level rainfall (throughfall adjustments)
  - Differences in data recording cadence over time (minute vs. hourly/half-hour averages)
- For further details or data requests beyond the EIDC entry, contact the project researchers listed in the documentation