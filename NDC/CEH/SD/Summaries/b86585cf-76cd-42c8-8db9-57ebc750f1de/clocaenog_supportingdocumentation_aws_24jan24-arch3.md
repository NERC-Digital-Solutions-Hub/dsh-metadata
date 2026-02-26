# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Data available from the Environmental Information Data Centre (EIDC): Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest. URL: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

- Data structure
  - Dataset: CLM_AWS_2022-2023_summaryQA.csv
  - Contains 10 columns and 731 rows; missing data marked as 'NA'; faulty data replaced by -9999
  - Columns include Date, Mean_air_temperature_degC, Minimum_air_temperature_degC, Maximum_air_temperature_degC, Rainfall_mm, Air_pressure_mbar, Solar_radiation_kW_per_m2, Photosynthetic_active_radiation_umol_per_m2_per_sec, Wind_speed_m_per_sec, Wind_direction_degrees

- Site information
  - Automated climate manipulation site established in 1998; replicates drought and warming treatments using automated roof technology powered by solar/wind
  - Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W); upland west-atlantic moorland with Calluna vulgaris (heather) dominant
  - Flora and soils
    - Vegetation includes Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
    - Soil: humo-ferric podzol with variable horizons; depth of eluvial and illuvial horizons (Eg/Bh) varies; C/N ratios and nutrient contents detailed in Table 4
  - Climate (1997–2014)
    - Mean annual air temp ~8.0°C; mean soil temp control plots ~7.5°C
    - Mean annual rainfall ~1411 mm
    - Total N deposition ~20–25 kg N ha⁻¹ yr⁻¹
  - Vegetation and soil characteristics summarized (e.g., annual litterfall ~177 g m⁻²; biomass data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes)

- Climate change treatment information
  - Treatments: drought and warming, each with three replicates; three control plots with scaffolding to mirror shading (9 plots total)
  - Drought treatment
    - Operation: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; May–Sept initially (1999–2011), later Apr–Oct (since 2012)
    - Rainfall reduction: ~20% annual; excluded rainfall during drought period ~80% due to sensor detection limits and roof coverage
    - Wind constraints: roofs do not operate in winds >10 m s⁻¹
  - Warming treatment
    - Operation: retractable aluminium mesh curtains to reduce infrared radiation; nighttime operation
    - Rainfall interaction: roofs retract when rain detected to preserve rainfall; some rainfall excluded due to lag
    - Wind constraints: similar limitations as drought treatment
  - Frame updates and maintenance
    - 2016–2017: replacement of aging frames; new frames installed June 2017 to minimize vegetation disturbance
  - Treatment timing and effectiveness
    - Detailed yearly data for drought and warming including dates of drought, percent rainfall reductions, and growing degree days (GDD) changes
    - GDD changes provided as percent change relative to control; data include years with incomplete records and notes on data gaps (e.g., sensor or rainfall data issues)
  - Data gaps and issues
    - Rainfall sensor on site broken since Jan 2018
    - Some years have missing or inferred data due to access restrictions or site conditions (e.g., COVID-related gaps)

- Equipment, protocols and data processing methodology
  - On-site equipment
    - Automated Weather Station (AWS) with meteorological sensors; additional micro-meteorological sensors within plots
    - Comprehensive data types collected include meteorology, soil/plant measurements, rainfall chemistry, throughfall, water table, soil respiration, trace gases, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter, roots, soil microbial biomass, nitrogen mineralisation, SOM, soil solution chemistry
  - Data management
    - Data summarized in Table 7; some datasets stored outside EIDC (post-2015 infrequent datasets)
    - Contacts for inquiries: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)
  - Data processing and quality control
    - AWS sensors sample every minute; hourly averages used
    - Basic quality control via visual inspection in Excel to identify trends and anomalies
    - Consistency notes: not all datasets are stored in centralized repositories; multiple data streams require cross-referencing and validation

- AWS Micro-meteorological data
  - Sensor types and measurements
    - Air temperature (HMP 45C)
    - Relative humidity (HMP 45C)
    - Solar radiation (Skye SP1110 pyranometer)
    - PAR (SKP215 Quantum Sensor)
    - Net radiation (NR-Lites)
    - Barometric pressure (CS100)
    - Rainfall (ARG100 tipping bucket)
    - Wind speed and direction (Windsonic 2D)
  - Data cadence and quality control
    - Measurements sampled every minute; hourly averages produced
    - Data QC performed with Excel-based checks to ensure data integrity and interpretability

- Storage rain gauge data (site-level rainfall) and rainfall chemistry
  - Rainfall measurement
    - Ground-level storage rain gauge (funnel 12.7 cm diameter); biweekly collection
    - Robust to logger/power interruptions; preferred when hourly data not required
  - Rainfall chemistry
    - Biweekly sampling of rainfall chemistry alongside rainfall volume

- Throughfall data (plot-level rainfall)
  - Throughfall collection
    - Plot-level rainfall captured biweekly using funnels and 3000 mL bottles
  - Data handling and reliability
    - Data require calculations to convert to plot-level rainfall; adjustments for losses (funnel detachment, bottle overflow, freezing)
    - Percent differences calculated relative to site rainfall to derive treatment means
    - Plot-level data may be excluded if data are compromised; infilling used sparingly with year-average reductions when necessary

- Appendix (figures)
  - Site layout and quadrat arrangement illustrated (figures referenced for layout and measurement areas)