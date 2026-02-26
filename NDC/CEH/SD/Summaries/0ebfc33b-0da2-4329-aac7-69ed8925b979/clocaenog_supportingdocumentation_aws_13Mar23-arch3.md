# Climoor field site in Clocaenog forest. Supporting documentation for data

## Purpose and context
- Climate change manipulation experiment (Clocaenog Forest, initiated 1998) using automated roof technology to simulate drought and warming for the next 20–30 years.
- Site supports environmental monitoring by providing long-term, controlled data on abiotic and biotic responses to climate treatments.
- Data designed to inform monitoring frameworks: measures, data quality, governance, and transparency.

## Data access, licensing and citation
- Data accessible at doi: https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- Licensing: Open Government Licence; users must cite Reinsch et al. (2022) when using the dataset.
- Dataset referenced: Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021 (NERC EDS Environmental Information Data Centre).

## Data structure
- Single data file: CLM_AWS_2016-2021_summaryQA.csv with 10 columns.
- Data quality marks: NA indicates not recorded; -9999 indicates faulty data replaced.
- Column descriptions cover:
  - Date (YYYY-MM-DD)
  - Mean air temperature (degC)
  - Minimum/Maximum air temperature (degC)
  - Rainfall (mm)
  - Air pressure (mbar)
  - Solar radiation (kW/m2)
  - Photosynthetically active radiation (µmol m-2 s-1)
  - Wind speed (m s-1)
  - Wind direction (degrees)

## Site information and ecological context
- Location: Clocaenog Forest, North East Wales; upland west-atlantic moorland; established 1998.
- Ecosystem and vegetation: dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum; bryophytes present; detailed plant species list and biomass data provided.
- Climate context (1997–2014):
  - Mean air temperature ~8.0°C; mean soil temperature in control plots ~7.5°C.
  - Mean annual rainfall ~1411 mm.
  - Total nitrogen deposition ~20–25 kg N ha-1 yr-1.
- Soil characteristics: humo-ferric podzol with variable horizons; notable C, N, base cations, CEC, and soil chemical properties tabulated.

## Climate change treatment information
- Treatments: drought and warming; each with three replicated plots; plus three control plots with scaffolding to mirror shading; total of 9 plots.
- Drought treatment:
  - Operational May–Sept (1999–2011); extended to Apr–Oct since 2012.
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor to reduce rainfall by ~20%; some rain events still excluded due to sensor limits.
  - Wind exclusion: roofs do not operate in winds > 10 m/s.
  - Frame reliability issues led to replacement/augmentation in 2017 (new frames installed June 2017 atop old ones).
- Warming treatment:
  - Night-time infrared radiation reduction via retractable aluminum mesh curtains; reduces heat loss at night by ~64%; curtains retracted during rain to avoid rainfall reduction.
  - Triggered by light level thresholds (e.g., after 15 minutes of darkness).
  - Rainfall reduction ~14% on an annual basis; wind and other constraints similar to drought treatment.
- Documentation includes per-year metrics (1997–2021) of drought/warming timing, rainfall reductions, and growing degree days (GDD) changes; formulation for calculating % change in warming effect provided.

## Equipment, protocols and data processing
- On-site automated weather station (AWS) plus micro-meteorological sensors within treatment plots; extensive abiotic and biotic data collected.
- Data types summarized (Table 7):
  - AWS meteorological data: relative humidity, air temp, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction (daily, 1999–present).
  - Plot-level micro-meteorological data: soil and air temperature, soil moisture (daily; some periods as hourly, then half-hourly post-2016).
  - Rainfall and rainfall chemistry: ground-level rain gauge (biweekly), plot throughfall (fortnightly), site-level rainfall used to derive plot-level rainfall.
  - Additional data: soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, soil organic matter, soil solution chemistry.
- Data quality control:
  - Basic visual QC in Excel to assess trends and anomalies; acknowledges trade-offs with automated limits.
  - Some datasets stored outside EIDC; inquiries coordinated through project contacts.
- Data access notes:
  - Some data not stored in EIDC; contact Sabine Reinsch or Bridget Emmett for further details.

## AWS and micro-meteorological details
- Sensor setup:
  - Air temperature and relative humidity: HMP 45C sensors (Campbell Scientific).
  - Solar radiation: Skye SP1110 pyranometer; PAR: SKP215 quantum sensor; Net radiation: NR-Lites.
  - Rainfall: ARG100 tipping bucket; wind: Windsonic 2D anemometer; barometric pressure: CS100.
- Data cadence:
  - Measurements captured every minute; hourly averages (AWS) or sub-hourly (micro-meteorological) data; post-2016 half-hour averages for some variables.
- Physical deployment notes:
  - AWS initially at 1 m height; moved to 4 m mast after thefts (2007) for security.

## Appendix and site layout
- Figures include:
  - Site layout and quadrat arrangement.
  - Quadrat-to-plot mapping and motor box locations.
- Quadrat layout: each quadrat is 0.5 m²; measurement areas defined for vegetation and related observations.

## Data governance and relevance for monitoring frameworks
- Licensing and citation requirements enable transparent reuse and policymaker scrutiny.
- Rich, multi-decade dataset capturing baseline conditions, treatment effects, and governance challenges (frame maintenance, rain-sensor limitations, data gaps).
- Documentation of data processing and QA practices provides a blueprint for data stewardship in monitoring frameworks.
- Variety of measured environmental health indicators (climate drivers, soil/vegetation responses, gas fluxes) supports evaluation of policy scenarios and adaptation strategies.