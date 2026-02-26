# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Available from the Environmental Information Data Centre (EIDC) under Data collection: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
  - Link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

- Data structure
  - A single dataset: CLM_AWS_2022-2023_summaryQA.csv with 10 columns and 731 rows.
  - Data quality flags
    - NA indicates not recorded
    - -9999 indicates faulty data replaced
  - Columns (example meanings)
    - Date (Year-Month-Day)
    - Mean_air_temperature_degC
    - Minimum_air_temperature_degC
    - Maximum_air_temperature_degC
    - Rainfall_mm
    - Air_pressure_mbar
    - Solar_radiation_kW_per_m2
    - Photosynthetic active radiation_umol_per_m2_per_sec
    - Wind_speed_m_per_sec
    - Wind_direction_degrees

- Site information
  - Location: Clocaenog Forest, North East Wales, UK (coordinates provided in the document)
  - Purpose: climate change manipulation experiment using automated roof technology to simulate drought and warming for the next 20–30 years
  - Establishment: 1998
  - Habitat: upland moorland with dominant Calluna vulgaris (heather); other species listed; bryophytes indicated
  - Soils: humo-ferric podzol with horizon details (Eg, Bh, etc.); soil properties include C, N, C:N, base saturation, CEC
  - Vegetation baseline (1998): shrub and bryophyte cover/biomass data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
  - Climate (1997–2014): mean temp ~8.0 °C; mean soil temp ~7.5 °C; mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha^-1 yr^-1

- Climate change treatment information
  - Treatments: drought and warming; each with three replicate plots; three control plots; total of 9 plots
  - Drought treatment
    - Implemented May–Sept (1999–2011); extended April–October since 2012
    - Method: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20%
    - Limitations: some small rain events missed; since 2016, rain accumulation on roof affected retraction
  - Warming treatment
    - Method: retractable aluminium mesh curtains; reflect 96–97% infrared radiation; reduces nighttime heat loss
    - Operation: activated after 15 minutes of darkness; roof retracts when rainfall detected to preserve rainfall
    - Rainfall effect: ~14% reduction in annual rainfall
  - Other operational notes
    - High wind (>10 m s^-1) prevents curtain operation to avoid damage
    - Frame maintenance: new frames installed on top of old ones in 2017 to minimize vegetation disturbance
    - 2016–2023: various interruptions (frame refurbishments, water on roofs causing retraction issues, COVID-19-related impacts)
    - Rainfall data gaps: site rainfall sensor broken since 04 Jan 2018; some years have incomplete data (marked with asterisks in the dataset)

- Equipment, protocols and data processing
  - Data types collected (Table 7 in the document)
    - AWS meteorological data (daily): temperature, humidity, rainfall, air pressure, net/solar radiation, PAR, wind speed/direction
    - Micro-meteorological plot data (daily): soil/air temperature, soil moisture
    - Rainfall data: ground-level storage gauge (biweekly); rainfall chemistry
    - Throughfall (plot-level rainfall): plot-level collection with funnels/bottles (biweekly); used to derive treatment-specific rainfall changes
    - Water table depth (fortnightly): permeable tubes
    - Soil respiration (fortnightly): IRGA measurements
    - Trace gases (CH4, N2O): closed static chambers
    - Net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, vegetation phenology and chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC
  - Data roles
    - Not all data are stored within EIDC; some datasets are infrequently collected or post-2015
    - For more details, contact project leads Sabine Reinsch or Bridget Emmett

- AWS micro-meteorological data specifics
  - Sensors and measurements
    - Air temperature: HMP 45C
    - Relative humidity: HMP 45C
    - Solar radiation: Skye SP1110 pyranometer
    - PAR: SKP215 Quantum Sensor
    - Net radiation: NR-Lites
    - Barometric pressure: CS100
    - Rainfall: ARG100 tipping bucket
    - Wind speed/direction: Windsonic 2D Ultrasonic Anemometer
  - Data cadence and QC
    - Measurements sampled every minute; hourly averages produced
    - Quality control via visual inspection in Excel (human-readable checks)

- Other meteorological data
  - Micro-meteorological plot data: soil temperature at 5, 10, 20 cm; soil moisture via TDR sensors (CS616) since 2008
  - Data cadence: minute-level; hourly or half-hourly averages after 2016
  - Data QC approach similar to AWS data

- Rain gauge and rainfall data (site-level and throughfall)
  - Site-level rainfall: ground-level storage rain gauge (biweekly measurements; robust against logger/power issues)
  - Throughfall data: plot-level rainfall collected biweekly; funnels/bottles with 3 L bottles
  - Data processing for rainfall
    - Throughfall percent differences are applied to site-level rainfall to derive plot-specific rainfall
    - If data are compromised (e.g., funnel falls off), the affected plot is excluded from treatment means; occasional infilling with year-average reductions may occur

- Appendix and site layout
  - Figures illustrating site layout and quadrat arrangement
  - Quadrat size: 0.5 m^2

- Data usage notes for GIS specialists
  - This dataset provides a rich, multi-Temporal, multi-layer climate and ecological context for the Clocaenog site
  - Useful for map-based visualization of drought/warming treatments, plot-level rainfall modifications, microclimate patterns, soil/vegetation characteristics, and long-term ecological responses
  - Be mindful of data gaps and treatment discontinuities (e.g., rainfall sensor failure, drought roof operation gaps, COVID-related interruptions) when designing analyses or visualizations

- Summary of end notes
  - The document documents comprehensive climate manipulation experiments at Climoor/Clocaenog (1998–present) with detailed data on climate, soils, vegetation, chemistry, and multiple ecological measurements
  - Data access is centralized through EIDC, with extensive metadata and caveats related to data completeness and instrument maintenance over time