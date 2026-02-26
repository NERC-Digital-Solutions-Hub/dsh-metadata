Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Data available from the Environmental Information Data Centre (EIDC) under the collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest. Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

- Data structure
  - Dataset: CLM_AWS_2022-2023_summaryQA.csv
  - Size: 28 columns, 731 rows
  - Data quality:
    - Missing values marked as NA
    - Faulty data replaced by -9999

- Site information
  - Location and purpose
    - Automated climate change manipulation site at Clocaenog Forest, North East Wales, established 1998
    - Reflects drought and warming treatments to simulate next 20–30 years of climate change
  - Habitat and vegetation
    - Upland west-atlantic moorland dominated by Calluna vulgaris (heather)
    - Other species include Vaccinium myrtillus, Empetrum nigrum; bryophytes common
    - Vegetation structure: high bryophyte cover; shrub and grass species present; annual litterfall ~177 g m-2
  - Soil
    - Humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons
    - Typical horizon depths and soil properties summarized in Table 2 (e.g., horizon Eg at 6–17 cm; Bh below)
  - Climate (1997–2014 context)
    - Mean air temp: 8.0°C; mean soil temp in control plots: 7.5°C
    - Mean annual rainfall: 1411 mm
    - Total N deposition: 20–25 kg N ha^-1 yr^-1
  - Vegetation and chemistry data included in site reports
    - Example vegetation chemistry metrics (C, N, C:N, P, K, Ca, Mg, lignin, tannin, α-cellulose, carbohydrates) across species and litter

- Climate change treatment information
  - Experimental design
    - Two treatments: drought and warming
    - Each treatment has three replicate plots (4 m × 5 m)
    - Three control plots with scaffolding to mirror shading; total 9 plots
  - Drought treatment
    - Timing: May–Sept (1999–2011); Apr–Oct (since 2012)
    - Mechanism: retractable polyethylene roof over 4 m × 5 m plot, triggered by tipping-bucket rainfall sensor
    - Effect: ~20% reduction in annual rainfall; ~80% of rainfall excluded within drought period due to sensor thresholds
    - Wind considerations: curtains do not operate in winds > 10 m s^-1
    - Operational notes: drought roof refurbishment and issues with water accumulation led to frame changes in 2017; rain-sensor robustness issues documented
  - Warming treatment
    - Mechanism: retractable aluminum mesh curtains at night; reflect 96–97% of IR, reducing nighttime heat loss by ~64%
    - Trigger: light sensor with a 15-minute dark period criterion; rain detected triggers roof retraction to preserve rainfall
    - Rainfall exclusion: some rainfall excluded due to lag between rain detection and roof retraction; ~14% annual rainfall reduction
    - Wind considerations: operations paused in high winds
    - Frame updates: new frames installed on top of old ones in June 2017
  - Treatment timing and efficacy data
    - Table 6 (a) drought and Table 6 (b) warming provide year-by-year dates and percent reductions in annual and growing-season rainfall
    - GDD (Growing Degree Days) calculations provided for warming vs control; recommended to use % change in GDD as data completeness varies
  - Data collection context
    - In some years, drought or warming data were interrupted (e.g., COVID-19-related interruptions in 2020–2021; 2016–2017 refurbishment; 2018 rain-sensor issues)

- Equipment, protocols and data processing methodology
  - Measurement infrastructure
    - Automated Weather Station (AWS) for meteorological data
    - Plot-level micro-meteorological sensors for abiotic and some biotic data
  - Data types and data scope
    - AWS meteorological data: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
    - Micro-meteorological (plot-level) data: soil and air temperature, soil moisture
    - Rainfall and rainfall chemistry: ground-level rain gauge and rainfall collectors
    - Throughfall data: plot-level rainfall via funnels and bottles
    - Additional data: soil respiration, trace gas measurements (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter and root biomass, soil organic carbon/biomass, soil solution/leachate chemistry
  - Data frequency and time-scale
    - Sensors: measurements at high frequency (per minute) with hourly or half-hourly averages for many variables
    - Throughfall and rainfall datasets updated fortnightly to monthly
  - Data quality control and processing
    - Basic quality control via visual inspection in Excel
    - Acknowledgement that automated QC can miss contextual anomalies; notes on data gaps and infill strategies
  - Data availability notes
    - Not all datasets stored in EIDC; some data collected after June 2015 are stored outside EIDC
    - Contact project leads for further details on infrequently collected or post-2015 datasets

- Micro-meteorological data – plot level data
  - Temporal resolution
    - Soil temperature: measured at 5, 10, and 20 cm depths
    - Soil moisture: currently using TDR sensors (volumetric water content); earlier methods included theta probes
  - Data recording
    - Measurements sampled every minute; logged as hourly averages up to Jan 2016, then half-hourly averages thereafter
  - Sensor details
    - AWS sensors mounted on a secure mast (initially 1 m above soil, later 4 m)
    - Measured variables include air temperature, relative humidity, solar radiation, PAR, net radiation, barometric pressure, rainfall, wind speed/direction
  - Data quality
    - Quality control described as visual/manual; data flagged with standard Excel-based checks

- Storage rain gauge data (site-level rainfall) and rainfall chemistry
  - Rainfall measurement
    - Ground-level storage rain gauge with 12.7 cm funnel; samples collected biweekly
    - Transfer and aggregation method ensures robust rainfall data, less prone to logger/power outages
  - Rainfall chemistry
    - Rain chemistry data collected concurrently with rainfall measurements

- Throughfall data (plot level rainfall)
  - Measurement method
    - Per-plot rainfall via a funnel (16.8 cm) and a 3000 mL bottle
  - Data handling
    - Throughfall data used to compute percent change relative to site-level rainfall
    - If data loss or field issues occurred (e.g., funnel detachments, bottles overflow), the plot is excluded from treatment means; infill used cautiously (e.g., average reductions across years)

- Appendix and site layout
  - Figures illustrating site layout and quadrat arrangement
  - Depictions of equipment frames, vents, and measurement areas

- Practical use for analysts
  - The dataset supports analyzing correlations between drought/warming treatments and abiotic/biotic responses at plot and site scales
  - Enables calculation of treatment-specific rainfall changes, GDD shifts, soil moisture/temperature responses, and consequent ecosystem processes (e.g., soil respiration, gas fluxes)
  - Data provenance and metadata are provided to enable reproducibility and discoverability, with clear notes on data gaps, QC methods, and transformations applied to the raw data