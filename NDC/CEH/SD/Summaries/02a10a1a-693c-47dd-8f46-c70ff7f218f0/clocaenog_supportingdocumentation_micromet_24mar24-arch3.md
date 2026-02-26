# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Data available from the Environmental Information Data Centre (EIDC)
  - Dataset: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest
  - Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

- Data structure and quality
  - One spreadsheet: CLM_AWS_2022-2023_summaryQA.csv
  - 28 columns, 731 rows
  - Missing entries marked as NA; faulty data replaced by -9999
  - Data quality: described QA process; some data not stored at EIDC; consult data owners for non-EIDC datasets

- Site overview
  - Climoor/Clocaenog climate change manipulation field site
  - Established 1998; automated roof technology to create drought and warming treatments
  - Location: Clocaenog Forest, North East Wales (upland moorland with Calluna vulgaris as dominant plant)
  - Soil: humo-ferric podzol with variable eluvial and illuvial horizons
  - Climate context (1997–2014): mean air temp ~8.0°C; mean control soil temp ~7.5°C; mean annual rainfall ~1411 mm; total N-deposition 20–25 kg N ha-1 yr-1
  - Vegetation and litter: diverse mosses and bryophytes; annual litterfall ~177 g m-2
  - Ecosystem and soil chemistry data are provided for multiple species and soil horizons

- Climate change treatment information
  - Treatments: drought and warming, each with three replicate plots; three control plots with scaffolding to mimic shading (total n=9 plots)
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor
    - Effect: reduces annual rainfall by ~20% on treatment plots
    - Timing: May–September (1999–2011); since 2012, April–October
    - Operational notes: some small rain events missed; from 2016, rainfall patterns caused accumulation on roofs preventing full retraction
  - Warming treatment
    - Mechanism: retractable aluminium mesh curtains; reflection of infrared radiation
    - Effect: night-time heat loss reduced; rain-triggered retraction to prevent rainfall bias
    - Operational notes: some rainfall exclusion persists due to retraction lag; curtains not used in winds >10 m s-1
  - Maintenance and evolution
    - Frame refurbishment and replacement occurred in 2017 (new frames installed atop old ones)
    - 2016–2017 frame issues affected long-term operation
  - Treatment detail records
    - Table 5: plot-to-treatment mapping
    - Table 6: year-by-year drought and warming details, including growing degree days (GDD) context and percent reductions
    - GDD changes are calculated from plot-level air temperatures; these provide a proxy for warming impact when complete data are unavailable

- Equipment, protocols and data processing methodology
  - Monitoring infrastructure
    - Automated Weather Station (AWS) for meteorological data
    - Micro-meteorological sensors within plots
    - Additional measurements: rainfall gauge, throughfall collectors, soil moisture sensors, soil temperature sensors, etc.
  - Data types and cadence
    - AWS sensors measure humidity, temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind (sampled every minute; hourly averages)
    - Plot-level micro-met data: soil/air temperature and soil moisture; originally varied methods; post-2008 use CS616 TDR sensors for soil moisture (m3/m3)
    - Data quality control: manual visual QC in Excel; acknowledges limitations of purely automated checks
  - Data catalog and scope
    - Table 7 summarizes data types collected at the site (e.g., meteorology, soil respiration, trace gases, canopy reflectance, vegetation surveys, litterfall, soil chemistry)
    - Not all data are stored at EIDC; contact authors for infrequently collected datasets or post-2015 data
  - Rainfall measurement and processing
    - Site rainfall: ground-level storage rain gauge (biweekly collection)
    - Plot rainfall: throughfall collectors (biweekly); data used to compute treatment-specific rainfall changes by applying percent changes to site rainfall
    - Data handling: if throughfall data are missing or compromised, the corresponding plot is excluded from treatment means; some infilling with average reductions used in rare cases

- Supplementary information
  - Appendix includes site layout and quadrat measurements (0.5 m² quadrats) to support spatial analyses
  - Figures referenced for site frame changes and rainfall throughfall considerations

- Practical implications for monitoring frameworks
  - Data accessibility and metadata
    - Central dataset available with clear structure; potential gaps where metadata are incomplete or not captured at the primary repository
  - Data quality and governance
    - Data quality relies on both automated and manual QC; explicit metadata about data provenance and processing steps is essential
    - Some datasets are not stored in the main data centre; ongoing governance should include data provenance, shareability, and provenance documentation
  - Measurement accuracy and harmonization
    - Multi-method changes (e.g., soil moisture sensors changing in 2008; sensor replacements) require careful harmonization and documentation for longitudinal policy evaluation
  - Treatment replication and comparability
    - Replicated design with clear treatment/control delineation supports robust impact assessment; detailed yearly treatment performance (e.g., drought reductions, warming GDD changes) aids policy-relevant modeling
  - Data gaps and resilience
    - Operational challenges (frame refurbishment, weather-related failures, equipment downtime, and COVID-related field access) illustrate the need for resilience planning and prospective data recovery strategies in monitoring frameworks