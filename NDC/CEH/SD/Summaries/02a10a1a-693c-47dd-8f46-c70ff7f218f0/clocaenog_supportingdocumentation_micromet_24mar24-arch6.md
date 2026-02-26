# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1. Overview
- Climate change manipulation experiment at Clocaenog Forest, initiated in 1998.
- Uses automated roof technology to produce drought and warming treatments to reflect predicted climate changes over 20–30 years.
- Includes replicated drought and warming treatments with control plots; aims to study ecosystem responses in upland moorland.

## 2. Data Access
- Data available from the Environmental Information Data Centre (EIDC) under the Data collection: Daily plot level (micro meteorological) data.
- Access point: Daily plot level data for Climoor field site in Clocaenog Forest (URL provided in documentation).

## 3. Data Structure
- Dataset: CLM_AWS_2022-2023_summaryQA.csv
- Contents: 1 spreadsheet, 28 columns, 731 rows.
- Data quality markers:
  - NA indicates missing data.
  - -9999 indicates faulty data.
- Example data elements include soil temperature at multiple depths and soil moisture across plots.

## 4. Site Information and Environment
- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W).
- Habitat: Upland moorland dominated by Calluna vulgaris (heather); bryophytes and other common species present.
- Soil: Humo-ferric podzol with variable horizons (E and Bh horizons described where apparent).
- Climate (1997–2014 in site report):
  - Mean air temperature: 8.0°C
  - Mean soil temperature (control plots): 7.5°C
  - Mean annual rainfall: 1411 mm
  - Total nitrogen deposition: 20–25 kg N ha-1 yr-1
- Vegetation: Dominant shrubs (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum) with a significant bryophyte component; annual litterfall ~177 g m-2.
- Vegetation and soil chemistry data provided for multiple plant species and litter, including C, N, P, K, Ca, Mg, lignin, tannin, cellulose metrics, and C:N ratios.

## 5. Climate Change Treatments
- Treatments: Drought and warming, each with three replicates (4 m x 5 m plots) plus three control plots (sham scaffolding to mirror shading), totaling 9 plots per treatment set.
- Drought treatment:
  - Operational May–September (1999–2011; extended/adjusted in later years).
  - Mechanism: Retractable polyethylene roofs triggered by rainfall sensors to exclude rainfall (~20% annual reduction; up to ~80% of rainfall excluded during drought periods due to sensor limits).
  - Since 2012–2016, timing adjustments and rainfall patterns caused changes; in 2016, rainfall accumulation on roofs impaired retraction.
- Warming treatment:
  - Retractable aluminium mesh curtains over warming plots; reflect infrared radiation to reduce heat loss at night (96–97% IR reflection; ~64% reduction in night-time heat loss).
  - Operated via light sensor; roofs retract when rain is detected to preserve rainfall; some rainfall excluded due to lag.
  - Wind limits: Curtains do not operate in high winds (>10 m s-1).
- Frame refurbishment:
  - 2017: New frames installed atop old ones to minimize vegetation disturbance.
  - Ongoing maintenance and occasional operational interruptions due to environmental conditions and equipment issues.
- Data context:
  - Rainfall reductions and growing degree days (GDD) calculated to quantify warming effects; cautions about incomplete data in some years due to site issues (sensor failures, COVID-19 impacts, etc.).

## 6. Equipment, Protocols and Data Processing Methodology
- Central data systems:
  - Automated Weather Station (AWS) for meteorological data (daily, site-wide).
  - Micro-meteorological (plot-level) sensors for soil and air temperature, soil moisture, etc. (daily; up to half-hourly after 2016).
- Data coverage:
  - AWS: measures relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Plot sensors: soil and air temperatures, soil moisture (TDR sensors installed since 2008; earlier manual theta probe methods).
  - Data quality control performed using manual inspection in Excel due to subjective data-context considerations.
- Data scope and storage:
  - Data types include AWS meteorology, plot-level soil/air data, rainfall (site level) and rainfall chemistry, throughfall data, water table depth, soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution and leachate chemistry.
  - Not all data are stored in EIDC after June 2015; some datasets require direct contact for access details.
- Temporal cadence:
  - Sensor data typically minute-level; hourly or half-hourly averages; plant/biomass measurements often annual or seasonal.

## 7. Data Quality, Gaps and Considerations
- Data completeness affected by:
  - Drought/warming infrastructure issues (roof operation failures, frame refurbishments).
  - Sensor reliability (rainfall gauge sensor issues; rainfall throughfall data gaps).
  - COVID-19 disruptions (field access in 2020–2021).
  - Site-specific issues with data logging and occasional missing years.
- Throughfall and rainfall data:
  - Throughfall measurements are biweekly; data quality carefully checked and exclusions applied when data integrity is compromised.
  - Throughfall-based seasonal/annual calculations are derived by applying percent changes to site-level rainfall data.
- Data users should account for:
  - Year-to-year changes in treatment operation and data availability.
  - Potential partial replication in treatment means when some plots are excluded due to data loss.

## 8. Use, Documentation and Contacts
- The dataset is well-suited for analyses of climate manipulation effects on upland moorland ecosystems, including soil moisture/temperature dynamics, hydrology, carbon fluxes, and vegetation responses under drought and warming scenarios.
- For more details or access to non-EIDC datasets, contact:
  - Sabine Reinsch
  - Bridget Emmett (enquiries@ceh.ac.uk)
- Appendix materials include site layout figures and quadrat/meter-scale measurement areas to contextualize plot-level data collection.