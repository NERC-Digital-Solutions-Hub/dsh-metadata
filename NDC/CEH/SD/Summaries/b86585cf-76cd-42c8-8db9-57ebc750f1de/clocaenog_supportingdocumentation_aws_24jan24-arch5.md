# Climoor field site in Clocaenog forest. Supporting documentation for data

- A climate change manipulation experiment at Climoor field site (Clocaenog forest) started in 1998, using automated roof technology to simulate drought and warming over 20–30 years. The dataset focuses on automated weather and micro-meteorological measurements, vegetation and site characteristics, and treatment implementation details.

## Data access
- Data available from the Environmental Information Data Centre (EIDC) under Data collection: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- Access link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99
- Metadata and data description are documented in this supporting file, with version: AWS - 24 Jan 2024.

## Data structure
- One primary spreadsheet: CLM_AWS_2022-2023_summaryQA.csv
- 10 columns and 731 rows
- Data gaps marked as NA; faulty data replaced by -9999
- Columns include:
  - Date (Year-Month-Day)
  - Mean_air_temperature_degC (Mean air temperature)
  - Minimum_air_temperature_degC (Minimum air temperature)
  - Maximum_air_temperature_degC (Maximum air temperature)
  - Rainfall_mm
  - Air_pressure_mbar
  - Solar_radiation_kW_per_m2
  - Photosynthetic active radiation_umol_per_m2_per_sec
  - Wind_speed_m_per_sec
  - Wind_direction_degrees

## Site information
- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W)
- Ecosystem: upland west-atlantic moorland, dominated by Calluna vulgaris (heather); bryophytes and other vascular plants present
- Climate (1997–2014): mean air temperature ~8.0°C; mean soil temperature ~7.5°C in control; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha-1 yr-1
- Soil: humo-ferric podzol with variable horizons (E and Bh; depths 6–17 cm observed where apparent); parent material Ordovician/Silurian shale or mudstone
- Vegetation characteristics: high Calluna vulgaris cover; bryophytes substantial; annual litterfall ~177 g m-2
- Vegetation and soil chemistry data included (C, N, C:N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates)

## Climate change treatment information
- Treatments: drought and warming, each with three replicates; plus three control plots (n=9 total)
- Drought treatment
  - Active May–September (1999–2011); years since 2012 adjusted to April–October
  - Mechanism: retractable polyethylene roof triggered by tipping bucket rainfall sensor; reduces annual rainfall by ~20%, excludes ~80% of rain during drought period
  - Rainfall sensor issues since 2018; some data gaps and operational changes due to rainfall accumulation on roof surfaces
- Warming treatment
  - Night-time warming using retractable aluminium mesh curtains; reflects 96–97% of infrared radiation, reducing nighttime heat loss
  - Roofs retracted during rain (sensor-triggered); average annual rainfall reduction ~14%
  - Operation controlled by light sensor and rain detection; weather conditions limit operation in wind >10 m s-1
- Structural updates
  - Original frames degraded; new frames installed on top of old ones in June 2017 to minimize vegetation disruption
- Data context
  - Table 6 (a) drought and Table 6 (b) warming provide year-by-year operation dates, rainfall reductions, and growing degree days (GDD) calculations
  - Treatment data span 1997–2023, with gaps due to frame refurbishments, COVID-19 disruptions, and sensor issues
- Notable data gaps and limitations
  - Drought roofs not operated from 2016 onward due to refurbishments and water on roofs
  - Rainfall sensor on site broken since Jan 2018
  - Some years marked with missing data or reduced field visits (COVID-19)
  - Data interpretation guidance suggests using percent change in GDD and incorporating known gaps

## Equipment, protocols and data processing methodology
- Data collection framework
  - Automated Weather Station (AWS) for meteorological data (daily); micro-meteorological (plot-scale) data collected since 1998
  - Additional data streams: ground-level rainfall, throughfall, water table depth, soil respiration, trace gases, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter and root biomass, soil and litter chemistry, and more
- AWS and micro-met data specifics
  - Sensors measure: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Measurements sampled every minute; hourly averages used (and later half-hourly averages from 2016)
  - Data quality control via visual inspection in Excel (human-in-the-loop approach)
- Rainfall data and processing
  - Site rainfall monitored by a ground-level storage rain gauge (biweekly data)
  - Plot-level rainfall captured via throughfall collection (per-plot funnels and bottles)
  - Data integration method: calculate plot-level rainfall by applying percent change (throughfall) to site-level rain gauge data; exclude plots with compromised data; infill rare cases using average reductions
- Data storage and accessibility
  - Some datasets (especially smaller or post-2015 datasets) not stored in EIDC; primary data access via EIDC for AWS-derived data and related documentation
  - For further details on infrequently collected datasets, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)
- Data processing notes
  - Throughfall and treatment-change calculations are essential for comparing per-plot rainfall against site rainfall
  - Table 7 provides a summary of data types stored and their storage location

## Data quality, governance and use considerations
- Data quality controls rely on manual verification in addition to automated checks; explicit data quality flags or thresholds are not documented
- Key governance points
  - Clear documentation of data structure, unit conventions, and missing value handling
  - Documentation of treatment implementations, frame replacements, and operational constraints relevant for reproducibility
  - Gaps and interruptions explicitly noted (frames refurbishment, heavy rainfall issues, sensor failures, COVID-19 impacts)
- Discoverability and reuse
  - Data are discoverable through the Environmental Information Data Centre
  - Metadata includes dataset scope, site characteristics, treatment details, instrumentation, sampling frequency, and data processing methods
  - Researchers should reference the Climoor/Clocaenog dataset with the provided contact points for access to additional data not in EIDC

- Contact for dataset breadth and details
  - Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for inquiries about non-EIDC data or dataset specifics not fully captured in the summary