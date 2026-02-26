# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access, licensing and citation
- Data accessible at https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
- License: Open Government Licence; by using the data you agree to the terms
- Citation: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre (Dataset)

## Data structure
- Dataset file: clm_micromet_2016-2021_summaryqa.csv (28 columns)
- Missing data marked as "NA"; faulty data replaced by "-9999"
- Content includes: soil temperature at 5 cm and 20 cm for multiple plots; soil moisture per plot

## Site information
- Location: Clocaenog Forest, North East Wales, UK; upland moorland with dominant Calluna vulgaris (heather)
- Climate and soils (1997-2014 context): mean air temp ~8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; soil humo-ferric podzol with variable eluvial/illuvial horizons
- Vegetation: shrub and bryophyte-dominated community; leaf C/N and nutrient metrics recorded for key species and litter
- Growing seasons: June–August peak; April–May and September–October shoulder seasons; winter dormancy
- Soil properties (various horizons) including C, N, C:N, base saturation, and exchange properties

## Climate change treatment information
- Treatments: drought and warming, each with three replicate plots (4 m × 5 m) and three controls (total 9 plots)
- Drought treatment
  - Operation: retractable polyethylene roof over plot during dry months
  - Timing: May–September (1999–2011); since 2012: April–October
  - Rain reduction: ~20% annual; deeper exclusion of ~80% of rainfall due to sensor limits
  - Notes: roofs may fail in high winds; 2016 refurbishment led to frame replacement in June 2017
  - 2016–2021: frames updated; some rainfall issues due to water on roof; later COVID-related disruptions
- Warming treatment
  - Operation: retractable aluminium mesh curtains over plots at night to reduce heat loss (reflects 96–97% IR)
  - Activation: after 15 minutes of darkness; rain-triggered retraction to preserve rainfall
  - Rain reduction: ~14% annual
  - Winds: curtains disabled in high winds
- Frame and maintenance
  - Original frames deteriorated; new frames installed on top of old ones in June 2017 to minimize vegetation disturbance
- Data context
  - Table 6(a) documents drought-year specifics (annual/seasonal rainfall reductions by year)
  - Table 6(b) documents warming-related growing degree days (GDD) changes by year
  - GDD calculations rely on plot-level air temperature data; NA where data missing

## Equipment, protocols and data processing methodology
- Monitoring and sensors
  - Automated Weather Station (AWS) for meteorological data (daily)
  - Micro-meteorological sensors in plots for soil and air temperature and soil moisture (daily)
  - Rainfall: ground-level rain gauge (biweekly) and plot-level throughfall collectors (biweekly)
  - Additional data: water table depth, soil respiration, trace gas measurements, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution chemistry
- Micro-meteorological data specifics
  - Soil temperature: T107 sensors at 5, 10, and 20 cm
  - Soil moisture: TDR sensors (CS616) installed from 2008; earlier manual theta probe measurements
  - Data collection: sensor measurements every minute; logged as hourly averages (pre-2016) and half-hourly averages (post-2016)
  - Data quality: basic QC via Excel-based visual checks
- AWS sensors and measurements
  - Air temperature, relative humidity, rainfall, air pressure, net/radiation, solar radiation, PAR, wind speed/direction
  - Sampling: every minute; outputs provided as hourly averages
- Rainfall and throughfall data
  - Site rainfall: biweekly storage rain gauge (robust to logger/power issues)
  - Throughfall: plot-level rainfall collected biweekly via funnels and bottles; data used to derive plot-level rainfall by applying percentage changes relative to site rainfall; data gaps treated as exclusions or infilled with average reductions when needed
- Data storage and access notes
  - Some datasets are not stored within the Environmental Information Data Centre (EIDC); contact authors for specifics
  - Data processing and QC methods are described; some manual QC approaches used due to site-specific nuances

## Data availability and usage notes for analysts
- Data accessibility: primary dataset and supporting data described; licensing and citation requirements apply
- Data gaps and caveats
  - Drought and warming data have inconsistencies across years due to sensor limitations, roof failures, heavy rainfall, high winds, refurbishment, and COVID-19-related disruptions
  - Some rainfall sensors have outages or data losses (e.g., rainfall sensor broken since 2018); throughfall data can be incomplete or require infilling
  - Not all data are stored at EIDC; verify availability with the contact points
- Data utility and integration
  - Rich, multi-year, plot-level micrometeorological data suitable for environmental health and climate manipulation analyses
  - Data structure supports standardised outputs (e.g., temperature, soil moisture, rainfall, and canopy/vegetation measurements)
  - Opportunities exist to increase dataset value by combining with other site data and enabling broader access to underlying data
- Publication and citation guidance
  - When using the dataset, cite the recommended reference and comply with licensing terms
  - Licensing and citation details provided in the data access section

## Appendix and figures
- Site layout and quadrat map provided (figures referenced in the appendix)
- Figures illustrate experimental plot arrangement, motor boxes, and frame configurations across time