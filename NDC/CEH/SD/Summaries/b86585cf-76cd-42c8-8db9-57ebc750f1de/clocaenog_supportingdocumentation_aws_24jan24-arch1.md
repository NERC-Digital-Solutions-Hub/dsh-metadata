# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Data available from Environmental Information Data Centre (EIDC) under the collection: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
  - Specific dataset referenced: CLM_AWS_2022-2023_summaryQA.csv (10 columns, 731 rows).
  - Data quality notes: missing values marked as NA; faulty data replaced by -9999.

- Data structure
  - One spreadsheet with 10 columns and 731 rows.
  - Columns (Date, Year-Month-Day; Mean_air_temperature_degC; Minimum_air_temperature_degC; Maximum_air_temperature_degC; Rainfall_mm; Air_pressure_mbar; Solar_radiation_kW_per_m2; Photosynthetic_active_radiation_umol_per_m2_per_sec; Wind_speed_m_per_sec; Wind_direction_degrees).
  - Data quality indicators: NA = missing; -9999 = faulty data.

- Site information and climate context
  - Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, 03°27'55"W).
  - Ecosystem: upland moorland dominated by Calluna vulgaris (heather); bryophytes present; typical plant community listed.
  - Soil: humo-ferric podzol with variable eluvial (Eg) and illuvial (Bh) horizons; depth and soil chemistry values provided (N, C, C:N, base cations, CEC).
  - Vegetation (1998 baseline data): Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes; annual litterfall ~177 g m-2; detailed biomass and chemistry data by species.
  - Climate (1997–2014): mean air temp ~8.0°C; mean soil temp in control plots ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha-1 yr-1.
  - Growing season and seasonal patterns described (growing: Jun–Aug; shoulder seasons; winter dormancy).

- Climate change treatment information
  - Experimental design: two treatments (drought and warming) with three replicates each, plus three control plots (total n=9 plots; 4 m x 5 m per plot).
  - Drought treatment: retractable polyethylene roof triggered by rainfall sensor; reduces annual rainfall ~20% (and ~80% of rain excluded during active drought window). Operational May–Sept (1999–2011); since 2012 Apr–Oct; since 2016 sometimes fails due to rainfall accumulation.
  - Warming treatment: retractable aluminum mesh curtains that reflect infrared radiation (96–97%), reducing night heat loss; rain-triggered retraction to limit rainfall loss; typically ~14% annual rainfall reduction.
  - Operational constraints: curtains do not operate in winds >10 m s-1 to prevent damage.
  - Infrastructure changes: frames refurbished/replaced by installing new frames on top of old ones (June 2017) to reduce vegetation disturbance.
  - Data gaps and issues: rainfall sensor failure since Jan 2018; some years affected by frame refurbishment, heavy rainfall on roofs, and COVID-19 related access restrictions (2020–2021).
  - Year-by-year treatment details are documented (Table 6a and 6b), including annual rainfall reductions and growing degree days (GDD) calculations for control and warming plots; GDD is used where temperature data are incomplete.

- Equipment, protocols and data processing methodology
  - Data collection infrastructure: automated weather station (AWS) on site plus plot-level micro-meteorological sensors; abiotic and biotic data collected within plots.
  - Data inventory (Table 7): AWS meteorological data (relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind); plot-level soil and air temperature and soil moisture; rainfall volume and chemistry; throughfall; water table depth; soil respiration; trace gas measurements (CH4, N2O); net ecosystem CO2 exchange; photosynthesis; vegetation surveys and canopy reflectance; vegetation phenology and pathogen assessments; vegetation chemistry; litterfall; root biomass; soil microbial biomass; nitrogen mineralisation; SOM and soil solution chemistry. Not all data are stored in EIDC post-2015; contact details provided for further data.
  - Data collection cadence and processing
    - AWS meteorological data: measured every minute; processed to hourly averages.
    - Micro-met plot data: daily measurements for soil/air temperature and soil moisture; logging formats changed over time (pre- and post-2016).
    - Rainfall data: site-level rain gauge (biweekly collection) preferred for robustness; throughfall collectors used per plot (biweekly); data adjusted to produce plot-level rainfall by applying percent-change differences relative to site rainfall; data gaps lead to exclusion or infill with average reductions.
  - Quality control: visual data checks in Excel; no strict automated flagging system described, enabling memory of conditions but potentially less rigorous than automated QC pipelines.

- AWS micro-meteorological data details
  - Sensor suite (examples): air temperature (HMP 45C), relative humidity, solar radiation (pyranometer), PAR (quantum sensor), net radiation, barometric pressure, rainfall (tipping bucket), wind speed/direction (Windsonic).
  - Positioning: initial sensors at 1 m above soil; moved to 4 m mast after thefts (2007).
  - Data cadence: 1-minute measurements, summarized as hourly or half-hourly in later years.
  - Data quality note: QC primarily via manual visual checks in Excel to preserve contextual understanding of site conditions.

- Rain gauge and throughfall data
  - Rain gauge: ground-level storage gauge, 12.7 cm funnel; two-week collection period; robust to logger/power interruptions; primary rainfall data source when hourly data are unnecessary.
  - Throughfall: plot-level rainfall captured with funnels and bottles (0.3 L capacity); data require processing to align with annual/seasonal rainfall totals; high-rainfall events can cause data loss; plots with compromised data are excluded from treatment means; infilling may use average reductions across years.

- Appendix and data visuals
  - Appendix includes site layout and quadrat layout figures, illustrating plot arrangement and monitoring areas.

- Practical implications for data users
  - The dataset enables analysis of climate manipulation effects on upland moorland ecosystems, including temperature and rainfall perturbations, canopy processes, soil moisture/chemistry, litter dynamics, and ecosystem gas exchange.
  - Data quality and completeness vary by year due to equipment refurbishment, sensor failures, and external disruptions (COVID-19); users should account for gaps and use caution with years affected by missing or partial data.
  - For integrated analyses, cross-reference AWS data with plot-level measurements (throughfall, soil respiration, gas fluxes) and document treatment status for each year.

- Data usage notes and contacts
  - Primary data steward contacts: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) at UKCEH Bangor.
  - Data are discoverable via the Environmental Information Data Centre (EIDC) with metadata and supporting documentation.