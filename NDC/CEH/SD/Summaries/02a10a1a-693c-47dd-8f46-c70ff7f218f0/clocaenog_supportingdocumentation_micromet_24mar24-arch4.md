# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Hosted by Environmental Information Data Centre (EIDC)
  - Dataset: Daily plot-level (micro meteorological) data for Climoor field site
  - URL: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

- Data structure
  - One CSV file: CLM_AWS_2022-2023_summaryQA.csv
  - 28 columns, 731 rows
  - Missing data marked as "NA"; faulty data replaced by -9999
  - Columns cover soil temperatures at multiple depths and plots, soil moisture, and other micro-meteorological variables
  - Data quality notes and QA information included

- Site overview
  - Climate change manipulation experiment initiated in 1998
  - Automated roof technology to simulate drought and warming for upland moorland
  - Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W)
  - Dominant vegetation: Calluna vulgaris (heather) with bryophytes and other vascular plants
  - Soil: humo-ferric podzol with variable horizons (Eg, Bh) and depths noted
  - Climate context (1997–2014): mean air temp ~8.0°C; mean control soil temp ~7.5°C; mean annual rainfall ~1411 mm; nitrogen deposition ~20–25 kg N ha⁻¹ yr⁻¹
  - Growing season: June–August; dormancy in winter; vegetation and litter data summarized for 1998 baseline

- Climate change treatment information
  - Treatments: drought and warming; each with three replicates plus three control plots (total 9 plots)
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by rainfall sensor
    - Timing: May–September (1999–2011); extended to April–October (since 2012)
    - Effect: ~20% reduction in annual rainfall; up to ~80% reduction in effective growing-season rainfall due to detection limits
    - Operational notes: roofs not used in high winds; refurbishments and rain accumulation issues led to changes and eventual replacement (2016–2017)
  - Warming treatment
    - Mechanism: retractable aluminum mesh curtains to reduce heat loss at night
    - Rainfall interaction: roof retraction upon rain detection; average ~14% annual rainfall reduction
    - Timing and operation tied to light/dark cycles; some years with overlapping operation with drought roofs
  - Maintenance and changes
    - Frames aged and required replacement; new frames installed on top of old ones (June 2017) to minimize vegetation disruption
    - 2016 refurbishment and ongoing maintenance affected treatment continuity
  - Yearly treatment data
    - Table 6a: drought-year details including annual rainfall and growing-season reductions
    - Table 6b: warming-year growth-degree-days (GDD) changes and operation notes

- Equipment, protocols and data processing
  - Data collection infrastructure
    - Automated Weather Station (AWS) for meteorology (daily)
    - Plot-level micro-meteorological sensors (daily)
    - Rainfall gauges (site-level) and throughfall collectors (plot-level)
    - Additional measurements: soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter, root and soil properties, and soil chemistry
  - Data storage and access
    - Not all data are stored at EIDC; some datasets are stored externally
    - For more details on less-frequently collected or post-June 2015 data, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)
  - Data processing and quality control
    - Micro-meteorological data: minute-resolution measurements aggregated to hourly or half-hourly (post-2016)
    - Visual quality checks performed in Excel; notes that automated QC limits may miss unusual events

- Micro-meteorological data – plot level
  - Sensor types and depths: soil temperature at 5, 10, and 20 cm; soil moisture via TDR sensors (2008 onward; earlier methods varied)
  - Sampling cadence: data logged every minute; hourly or half-hour averages
  - QC approach: manual visual inspection to identify trends and anomalies

- Rainfall data and rainfall chemistry
  - Site rainfall: storage rain gauge (biweekly collection; more robust than AWS during outages)
  - Throughfall: plot-level rainfall collected biweekly using funnels and bottles
  - Data handling: throughfall-based percent changes applied to site rainfall to estimate plot-level rainfall; compromised data excluded from treatment means; occasional infilling with average reductions when needed

- Appendix and figures
  - Site layout and quadrat plots illustrations accompany the documentation

- Key data use considerations for data leadership
  - Complex, multi-source data ecosystem requiring careful metadata management and data lineage
  - Treatment effects depend on accurate alignment of drought and warming timelines with meteorological data
  - Data gaps due to maintenance, weather-related issues, and COVID-19 necessitate clear documentation of missing periods
  - Contact points provided for data inquiries and detailed dataset discovery

- Contacts
  - Sabine Reinsch (Sabine.Reinsch@ceh.ac.uk)
  - Bridget Emmett (Bridget.Emmett@ceh.ac.uk)