# Climoor field site in Clocaenog forest. Supporting documentation for data

- Overview: Describes the Climoor/Clocaenog climate change manipulation field site (established 1998) that uses automated roof technology to create drought and warming treatments simulating predicted climate conditions. Provides data access, structure, site characteristics, treatment details, and data collection/processing methods.

## Data access
- Data hosted by Environmental Information Data Centre (EIDC) under the Data collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest.
- Access link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## Data structure
- Dataset consists of a single spreadsheet: CLM_AWS_2024_summaryQA.csv
  - 28 columns, 367 rows
  - Recorded values marked as "NA" if not recorded; faulty data replaced by -9999
- Data categories include:
  - Date (Year-Month-Day)
  - Soil temperature at 5 cm depth for multiple plots
  - Soil temperature at 20 cm depth for multiple plots
  - Soil moisture (volumetric water content) per plot
  - Descriptions/units included (e.g., °C for temperature, m3/m3 for soil moisture)

## Site information
- Location: Clocaenog Forest, North East Wales, UK (upland moorland habitat)
- Establishment: 1998; automated manipulation site delivering drought and warming treatments
- Habitat and vegetation: Dominated by Calluna vulgaris (heather) with Vaccinium myrtillus, Empetrum nigrum, and bryophytes; rich bryophyte cover; soil: humo-ferric podzol
- Climate context (1997–2014 data): Mean air temp ~8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; N deposition ~20–25 kg N ha-1 yr-1
- Soil characteristics (across horizons Oh, Eg, Bh): Data include soil chemical properties (C, N, P, K, Ca, Mg, Al, H+), CEC, base saturation, and horizon-specific values
- Vegetation and chemistry: Baseline litterfall and biomass; species composition; vegetation chemistry data (C, N, C:N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates)

## Climate change treatment information
- Treatments: Drought and warming, each with three replicated plots; plus three control plots (scaffold-mirrored shading) for a total of nine plots
- Drought treatment
  - Mechanism: Retractable polyethylene roof triggered by tipping-bucket rainfall sensor
  - Effect: Reduces annual rainfall by ~20%; excludes ~80% of rainfall during active drought months
  - Timings: Primarily May–September (varied over years; since 2012 Apr–Oct; 2016 adjustments due to rainfall patterns)
- Warming treatment
  - Mechanism: Retractable aluminium mesh curtains that reflect 96–97% IR, reducing night heat loss
  - Control: Curtain operation based on light sensor; retracts if rain detected to preserve rainfall
  - Effect: Annual rainfall reduction ~14%
  - Wind restriction: Curtains do not operate in winds >10 m s-1
- Maintenance and changes
  - Frame and mechanism aging led to failures; 2016 refurbishment
  - New frame installation atop old frames in 2017 to minimize vegetation disruption
- Data context and gaps
  - Rainfall sensors and throughfall data issues (e.g., 2018 sensor failure; COVID-era access affecting fieldwork)
  - Throughfall and rainfall data processing uses site rainfall as baseline with plot-level adjustments; occasional data gaps or infilling with year-average reductions
- Growing Degree Days (GDD)
  - Calculated for control and warming treatments; used to quantify warming effect over years
  - Method uses plot-based air temperature data; provides percent change in GDD due to warming

## Equipment, protocols and data processing methodology
- Data collection framework
  - Automated Weather Station (AWS) for meteorology; plot-level micro-meteorological sensors
  - Additional abiotic/biotic data streams from within plots
  - Data storage and sharing via CEH/UKCEH resources; contact Sabine Reinsch or Bridget Emmett for details
- Micro-meteorological data (plot-level)
  - Temperature: Soil temperature measured at 5, 10, and 20 cm depths; sensors include Campbell Scientific T107
  - Soil moisture: TDR CS616 sensors installed since 2008 (volumetric water content, m3/m3); earlier data from manual probes
  - Sampling cadence: Measurements every minute; hourly averages up to Jan 2016; half-hourly averages after Jan 2016
  - Data quality: QC performed via basic Excel-based visual checks
- AWS meteorological data
  - Sensors cover: Air temperature, relative humidity, rainfall (tipping bucket), net/radiation, solar radiation, PAR, wind speed/direction, barometric pressure
  - Sampling cadence: Minute-level measurements; hourly averages
  - Data quality: QC via manual visual checks; historically vulnerable to logger/power issues
- Rainfall and rainfall chemistry
  - Site rainfall: Ground-level storage rain gauge; biweekly samples; robust to logger downtime
  - Throughfall: Plot-level rainfall captured biweekly using funnels and bottles; data adjusted to derive plot-level rainfall by applying percent changes relative to site rainfall; data losses lead to exclusion from treatment means or infilling with year-average reductions
- Data processing notes
  - Data normalization and processing rely on documented methods; some data infilling and exclusion rules applied when measurements are missing or compromised

## Data accessibility and contact
- Primary access through CEH Environmental Information Data Centre (EIDC)
- For additional details or infrequent datasets (post-2015), contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)

## Key considerations for data users
- Data completeness: Several years show gaps due to equipment failures, refurbishment, or external disruptions (e.g., COVID-19)
- Data quality: Manual QC practices used; some potential for unflagged anomalies exists due to lack of automated QC thresholds
- Metadata and lineage: Extensive site and treatment metadata available (treatment layouts, plot mappings, service logs, GDD calculations)
- Reproducibility: Clear documentation of measurement methods, sensor types, units, and processing steps supports reproducibility of analyses and meta-analyses across sites
- Data integration: Multiple data streams (AWS, micro-meteorological, rainfall, throughfall, soil properties) require careful alignment by time stamps and plot identifiers for integrated analyses