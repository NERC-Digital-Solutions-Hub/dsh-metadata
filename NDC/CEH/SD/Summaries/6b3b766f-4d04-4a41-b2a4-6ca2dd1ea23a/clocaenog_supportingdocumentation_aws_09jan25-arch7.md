# Climoor field site in Clocaenog forest. Supporting documentation for data

- Overview
  - A climate change manipulation experiment initiated in 1998 at Clocaenog Forest, North Wales, using automated roof technology to simulate drought and warming for the coming decades.
  - Data are archived at the Environmental Information Data Centre (EIDC), under the collection “Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.”

- Data access
  - Primary data access: Environmental Information Data Centre (EIDC) – CLMOOR AWS dataset summary (CSV) and related documentation.
  - Specific data file referenced: CLM_AWS_2024_summaryQA.csv (10 columns, 367 rows). See data collection page for details.

- Data structure and content (AWS dataset)
  - File: CLM_AWS_2024_summaryQA.csv
  - Columns (with units): 
    - Date (Year-Month-Day)
    - Mean_air_temperature_degC (degC)
    - Minimum_air_temperature_degC (degC)
    - Maximum_air_temperature_degC (degC)
    - Rainfall_mm (mm)
    - Air_pressure_mbar (mbar)
    - Solar_radiation_kW_per_m2 (kW/m2)
    - Photosynthetic active radiation_umol_per_m2_per_sec (µmol m-2 s-1)
    - Wind_speed_m_per_sec (m/s)
    - Wind_direction_degrees (degrees)
  - Data quality: missing values marked as NA; faulty data replaced by -9999.

- Site context
  - Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W).
  - Ecosystem: upland west-Atlantic moorland, dominated by Calluna vulgaris (heather); bryophytes present in several plots.
  - Vegetation and soils: diverse shrub, bryophyte and heather components; humo-ferric podzol with variable eluvial (Eg) and illuvial (Bh) horizons.
  - Growing season: June–August (main), with shoulder seasons Apr–May and Sep–Oct; winter dormancy Nov–Feb.
  - Representative soil/foliar chemistry and litter data provided in accompanying tables (e.g., C, N, C:N, mineral nutrients, lignin/tannin fractions).

- Climate (historical context)
  - Climate characteristics (1997–2014): mean air temp ~8.0°C; mean soil temp in control plots ~7.5°C; mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha^-1 yr^-1.

- Climate change treatment information
  - Treatments: drought and warming, each with three replicate plots; plus three control plots with scaffolding to mirror shading (9 plots total).
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by a tipping-bucket rainfall sensor to reduce rainfall on treatment plots; historically ~20% reduction in annual rainfall; larger effect on growing-season rainfall (up to ~80% reduction during certain years).
    - Timing: May–Sept (1999–2011), expanded to Apr–Oct from 2012 onward; operation halted during high winds (>10 m s^-1).
    - Changes/maintenance: frames refurbished/replaced in 2017; some water accumulation on roofs affected retractability; drought roofs not operated from 2016 onward due to refurbishments and then water-related issues.
  - Warming treatment
    - Mechanism: retractable aluminum mesh curtains to reduce nighttime heat loss; reflects 96–97% of infrared radiation.
    - Operation: roofs retract in the presence of rain to avoid reducing rainfall; nighttime warming cycles triggered after a defined dark period; wind limits apply.
    - Rainfall impact: approx. 14% annual rainfall reduction.
  - Frame maintenance and operational notes
    - Original framing ageing prompted installations of new frames atop old ones in June 2017 to minimize vegetation disturbance.
    - Drought-related and rainfall-related operational changes documented; 2016–2017 frame upgrades and rainwater issues noted.
  - Data gaps and notes
    - Rainfall sensor on site broken since Jan 2018.
    - Data gaps due to COVID-19 restrictions in 2020–2021 and other years; some drought years not fully recorded or infill used.
    - Appendix tables detail year-by-year drought and warming operational periods and percent rainfall reductions.

- Equipment, protocols and data processing (data collection and handling)
  - AWS (Automated Weather Station)
    - On-site meteorological data (AWS met data) collected daily; sensors provide 1-minute samples, averaged hourly.
    - Sensors include: air temperature, relative humidity, rainfall, air pressure, net/radiation/solar radiation, PAR, wind speed and direction.
    - Quality control primarily manual (visual checks in Excel) to assess trends and anomalies; automated limits not universally applied.
  - Micro-meteorological plot data
    - Plot-level soil and air temperature (5, 10, 20 cm) and soil moisture (TDR sensors installed 2008; earlier methods varied).
    - Data are collected frequently (daily to sub-daily), stored as hourly (pre-2016) or half-hourly averages (post-2016).
  - Rainfall data
    - Site-level rainfall: automated storage rain gauge; biweekly data; recommended as the most robust dataset when hourly data are not required.
    - Throughfall data: plot-level rainfall collected biweekly via funnels and bottles; used to compute percent change relative to site rainfall; data gaps handled by excluding affected plots or infilling with year-average reductions when necessary.
  - Other data types (listed in Table 7)
    - Rainfall chemistry, soil respiration, trace gas measurements (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC/bulk density, soil solution chemistry, among others.
    - Not all data are stored in the EIDC after June 2015; some details and datasets require direct contact for access.

- GIS-appropriate data products and layers
  - Potential layers derived from the dataset:
    - AWS meteorological layer: daily/hourly climate surfaces (temperature, rainfall, humidity, wind, radiation) for site.
    - Micro-meteorological plot layer: soil temperature, soil moisture by depth, plot-scale microclimate rasters.
    - Rainfall and throughfall layers: plot-level rainfall contributions vs site rainfall; throughfall loss percentages by plot and year.
    - Climate treatment layer: plot annotations for drought, warming, and control treatments with replication (9 plots total).
    - Vegetation and soil layers: vegetation cover/biomass, species composition, litterfall, litter and soil chemistry profiles, soil horizon characteristics.
    - Ecosystem flux layers: NECO2, soil respiration, trace gas fluxes (CH4, N2O) with plot associations.
    - Canopy and phenology layers: canopy reflectance indices, phenological measures, annual growth metrics.
  - Spatial notes: precise site location coordinates provided; field layout and quadrat-based plotting described (appendix figures).

- Data quality, limitations, and guidance for use
  - Data completeness varies by year; some years marked with missing or questionable data.
  - Drought and warming treatments experienced operational interruptions due to frame maintenance, water accumulation, high winds, COVID-19, and sensor issues.
  Data users should:
    - Check the CLM_AWS_2024_summaryQA.csv QA notes for missing/faulty entries.
    - Be cautious with years 2016 onward for drought data (frame upgrades, roof issues) and 2018 onward for rainfall sensor reliability.
    - Consider avoiding or treating with care years where throughfall or rainfall data were incomplete or heavily infilled.
  - Data provenance: primary AWS data and documentation are housed at EIDC; for non-EIDC datasets (post-2015 or infrequently collected data) contact the authors or UKCEH Bangor for access and details.

- Contacts and additional information
  - Primary author: Sabine Reinsch
  - Data inquiries: enquries@ceh.ac.uk (Sabine Reinsch or Bridget Emmett) for details on datasets not stored at EIDC or for dataset specifics.

- Spatial and temporal context for GIS projects
  - Spatial context: upland moorland site with well-documented climate manipulation plots; coordinates and site layout available in the accompanying appendix.
  - Temporal context: datasets span 1997–present (with gaps due to maintenance, COVID, and sensor issues); several variables captured daily to sub-daily, with some datasets collected biweekly or seasonally.