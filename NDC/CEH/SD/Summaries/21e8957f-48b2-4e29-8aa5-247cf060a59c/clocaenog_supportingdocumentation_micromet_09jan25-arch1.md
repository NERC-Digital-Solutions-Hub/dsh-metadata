# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Available from the Environmental Information Data Centre (EIDC) under the collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest.
  - Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

- Data structure
  - One CSV file: CLM_AWS_2024_summaryQA.csv
  - 28 columns and 367 rows
  - Missing data marked as "NA"; faulty data replaced by "-9999"

- Site information
  - Automated climate change manipulation site (Clocaenog Forest, North East Wales) established in 1998
  - Habitat: upland moorland; Calluna vulgaris dominates (>60% biomass)
  - Plant community includes Vaccinium myrtillus, Empetrum nigrum, and bryophytes; typical species list provided
  - Soil: humo-ferric podzol; variable horizons (Eg, Bh) with depths around 6–17 cm for Eg and below Bh
  - Climate (1997–2014): mean air temperature ~8.0°C; mean soil temperature in control ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha-1 yr-1

- Climate and soil characteristics
  - Vegetation and biomass data from 1998 baseline
  - Soil chemical properties and C:N, base cations, and other metrics summarized by horizon (LF, Oh, Eg, Bh)

- Climate change treatment information
  - Treatments: drought and warming; each with three replicated plots (4 m x 5 m); three control plots with scaffolding to mirror shading
  - Drought treatment
    - Operated annually May–September (1999–2011); later extended or adjusted (April–October since 2012)
    - Mechanism: retractable polyethylene roof triggered by rainfall sensor; reduces annual rainfall by ~20% (and ~80% of rain during active drought periods)
    - Operational constraints: not used in high winds (>10 m s-1); 2016 refurbishment and 2017 installation of new frames
  - Warming treatment
    - Nighttime warming via retractable aluminum mesh curtains; reflects 96–97% of infrared radiation
    - Rainfall management via tipping bucket sensor; rain can cause retraction to minimize rainfall loss; overall ~14% annual rainfall reduction
    - Curtains not operated in high winds; occasionally leads to rainfall exclusion
  - Temporal details and changes
    - Drought operation paused or adjusted due to frame refurbishments and roof water accumulation (2016–2017) and COVID-19 impacts
    - New frame installation in 2017; later years show variable operation (Table 6 notes)
  - Rainfall/GDD metrics
    - Growing Degree Days (GDD) calculated for control vs. warming treatments; method and yearly values provided
    - GDD changes used to quantify warming impact; emphasized that GDD values are averages across three replicates

- Equipment, protocols and data processing methodology
  - On-site automated weather station (AWS) plus plot-level micro-meteorological sensors
  - Data types collected (examples)
    - Meteorological: air temperature, relative humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
    - Plot data: soil and air temperature at multiple depths, soil moisture (TDR sensors installed 2008, earlier methods prior to 2008)
    - Additional measurements: rainfall throughfall, water table depth, soil respiration, trace gas fluxes, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litterfall, root and microbial biomass, soil organic matter and chemistry
  - Sensor specifics
    - AWS sensors and brands (e.g., HMP 45C, Skye SP1110, SKP215, NR-Lites, ARG100, Windsonic)
    - Plot sensors include T107 soil temperature probes and CS616 TDR soil moisture probes
  - Data cadence and QA
    - Most sensors sample every minute; hourly or half-hour averages used for analysis
    - Initial quality control via visual Excel checks; acknowledges limitations of manual QA vs automated QC
  - Data storage and accessibility
    - Some datasets stored outside EIDC, especially infrequent or post-2015 data
    - Contact project leads for detailed dataset availability and scope

- Micro-meteorological data – plot level
  - Plot-level measurements collected since 1998–2008 (with continuous daily/monthly records since 1999)
  - Soil temperature at 5 cm, 10 cm, 20 cm depths; soil moisture (CS616 TDR) installed in 2008
  - Data quality and handling
    - Data logged as minute-scale and summarized to hourly or half-hour averages after 2016
    - Ongoing QA uses non-automated approaches in early years; manual checks documented

- Storage rain gauge data (site-level rainfall) and rainfall chemistry
  - Ground-level rain gauge (funnel 12.7 cm) with biweekly collection
  - Rainfall data considered more robust than AWS data due to logger power and downtime resilience
  - Rainfall throughfall data collected biweekly (funnel 16.8 cm; 3,000 mL bottles)
  - Seasonal/annual rainfall for treatments derived by applying percent-change reductions from throughfall to site-level rainfall; data loss results in plot exclusion or infill with year-wide averages

- Throughfall data and data processing
  - Throughfall measurement challenges: overflow, bottles blown over, funnel detachment
  - Calculation approach: use throughfall percent difference to adjust site rainfall per treatment; exclude plots with compromised data; infill when appropriate

- Appendix and site layout
  - Figures illustrate site layout and plot/quadrat arrangement
  - Each quadrat is 0.5 m²
  - Descriptions of plot numbering and motor box locations included for reference

- Practical considerations for analysis
  - Data gaps and quality issues to account for: NA/-9999 values, roof operation gaps due to refurbishments and weather, COVID-19 restrictions
  - Spatial replication and long time series enable correlations between warming/drought treatments and soil/vegetation responses
  - Availability of metadata and methods enables reproducible analyses and dataset discovery via metadata portals

- Summary of potential analyses
  - Compare soil temperature and soil moisture across warming, drought, and control plots at multiple depths
  - Assess rainfall manipulation effectiveness by examining throughfall vs. site rainfall and corresponding soil/vegetation responses
  - Explore relationships between climate treatment intensity (e.g., % rainfall reduction, GDD changes) and ecological metrics (vegetation composition, litterfall, soil chemistry)
  - Integrate AWS and micro-meteorological data with plot-level measurements to model ecosystem CO2 fluxes and respiration under altered moisture and temperature regimes