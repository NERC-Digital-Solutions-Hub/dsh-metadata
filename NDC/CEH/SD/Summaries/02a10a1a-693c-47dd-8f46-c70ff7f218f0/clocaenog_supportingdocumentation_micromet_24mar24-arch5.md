# Climoor field site in Clocaenog forest. Supporting documentation for data

- Access to data is via the Environmental Information Data Centre (EIDC) under the data collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest. Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b
- Primary dataset file: CLM_AWS_2022-2023_summaryQA.csv (28 columns, 731 rows)
  - Date format: Year-Month-Day
  - Variables include soil temperature at 5 cm and 20 cm for multiple plots, soil moisture for plots, and related environmental measurements
  - Missing data: recorded as "NA"; faulty data replaced by "-9999"
  - Data quality and provenance: some data quality control notes provided; not all data may be stored in EIDC (from 2015 onward)
- Data availability notes
  - Not all data are stored within EIDC; for infrequently collected datasets or post-June 2015 data, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for details
  - Appendix includes site layout and quadrat mapping for measurement areas

## 2. Data structure and file formats

- Data file: CLM_AWS_2022-2023_summaryQA.csv
  - 28 columns representing variables such as soil temperature at various depths, plot-specific measurements, and related descriptors
  - 731 rows representing daily observations
  - Example descriptors include:
    - TSoil5cm_PlotX_degC: soil temperature at 5 cm depth for plot X
    - TSoil20cm_PlotX_degC: soil temperature at 20 cm depth for plot X
    - Soil_moisture_PlotX_m3_per_m-3: volumetric soil moisture for plot X
- Data usage and cleaning notes
  - NA indicates missing data
  - -9999 indicates previously recorded faulty data that has been replaced
  - Data might require cleaning or interpretation when used for analyses

## 3. Site context and climate change treatment information

- Location and site characteristics
  - Clocaenog Forest, North East Wales, UK (upland moorland with Calluna vulgaris-dominated vegetation)
  - Automated drought and warming treatments designed to simulate climate change scenarios
- Treatments and replication
  - Two climate change treatments: drought and warming
  - Each treatment has three replicate plots; three control plots (total 9 plots)
  - Warming and drought mechanisms described (retractable roofs/curtains; solar/wind power)
- Treatment timing and evolution
  - Drought treatment active May–Sept (1999–2011); extended to Apr–Oct since 2012
  - Warming treatment activated at night using retractable aluminium mesh curtains
  - Rainfall management includes a tipping bucket rainfall sensor and guard against high winds
  - Since 2016, drought roofs faced issues with water pooling; new frame installations occurred in 2017 to minimize vegetation disturbance
  - Rainfall measurements: rainfall sensor issues include a broken sensor since 2018
  - COVID-19 impacts: field work restrictions affected data collection in 2020–2021
- Climate and soil context (selected insights)
  - Climate regime (1997–2014) data summarized: mean air temp ~8.0 °C; mean soil temp in control ~7.5 °C; mean annual rainfall ~1411 mm
  - Soil: humo-ferric podzol with variable eluvial and illuvial horizons (Eg, Bh horizons observed in places)
  - Vegetation: dominant shrubs and bryophytes; bryophytes prominent in 1998 baseline measurements

## 4. Data collection, instrumentation, and processing

- Instrumentation and data sources
  - Automated weather station (AWS) for meteorological data (daily, minute-level to hourly averages)
  - Micro-meteorological plot sensors for soil and air temperature, soil moisture, rainfall, net radiation, PAR, wind, etc.
  - Additional data streams include rainfall chemistry, throughfall, soil respiration, trace gases, canopy reflectance, litterfall, vegetation surveys, and more
- Data collection cadence and processing
  - Plot-level micro-meteorological data logged at high frequency (minutes); hourly or half-hour averages produced after 2016
  - AWS sensors mounted on a reinforced mast after thefts; detailed sensor types and locations listed
  - Quality control historically performed in Excel due to practical considerations, with visual inspection of trends rather than automated thresholding
- Rainfall data specifics
  - Site rainfall measured with a ground-level storage gauge (biweekly collection)
  - Throughfall data collected biweekly per plot using funnels and bottles; data used with a normalization approach to derive per-treatment rainfall from site rainfall
  - Data gaps and data loss acknowledged (e.g., funnel bottle losses, overflow, or damaged equipment) with occasional infill using average reductions

## 5. Data processing methodology and governance notes

- Data processing and QC
  - Micro-met data include sensor-specific processing (soil temps at multiple depths; soil moisture via TDR sensors since 2008; earlier theta probe measurements)
  - Data processing notes emphasize manual QC approaches and documentation of data quality concerns
- Data storage and accessibility
  - Primary dataset (CLM_AWS_2022-2023_summaryQA.csv) stored with accompanying metadata; additional micro-met, rainfall, and related datasets may be stored outside EIDC
- Governance and contact points
  - Primary contact for questions about non-EIDC datasets: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)
  - Users should reference the dataset and site context when requesting additional data (e.g., post-2015 measurements, post-2018 sensor issues, or COVID-related gaps)

## 6. Key takeaways for data stewardship

- A comprehensive, high-resolution climate manipulation dataset exists for Climoor/Clocaenog, with a focus on drought and warming treatments and a suite of meteorological, soil, and ecosystem measurements
- The principal data asset is a CSV file (CLM_AWS_2022-2023_summaryQA.csv) with 28 variables across 731 daily observations, including explicit handling of missing and faulty data
- Data governance notes highlight incomplete data preservation within EIDC for earlier years and post-2015 data, plus ongoing caveats due to equipment issues and pandemic-related disruptions
- For robust reuse, users should integrate the treatment structure (nine plots with replicated drought, warming, and control conditions), account for data gaps (sensor outages, COVID years), and apply the documented methods for deriving plot-level rainfall from site-level measurements
- When combining datasets (e.g., micro-met data, rainfall, and throughfall), ensure consistent temporal alignment and quality thresholds, and consult the listed contacts for access to non-EIDC datasets or historical data not included in the main CSV