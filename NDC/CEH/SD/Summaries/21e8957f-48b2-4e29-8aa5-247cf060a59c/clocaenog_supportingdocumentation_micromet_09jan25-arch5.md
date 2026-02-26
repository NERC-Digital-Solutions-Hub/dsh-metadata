# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access
- Data are accessible via the Environmental Information Data Centre (EIDC) under Data collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest.
- Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## Data structure
- Dataset: CLM_AWS_2024_summaryQA.csv
- Contains 28 columns and 367 rows.
- Missing data marked as "NA"; faulty data replaced by "-9999".
- Columns include soil temperature at 5 cm and 20 cm for multiple plots, soil moisture (m3/m-3), dates, and descriptions for each plot (e.g., TSoil5cm_Plot1_degC, Soil_moisture_Plot1_m3_per_m-3, etc.).

## Site information
- Climoor/Clocaenog field site is an automated climate-change manipulation experiment (established 1998) using drought and warming treatments.
- Location: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W); upland moorland with Calluna vulgaris (heather) dominance.
- Automated roof technology powered by solar and wind; replicated drought and warming treatments with controls.
- Soil: humo-ferric podzol with variable horizon development (E and Bh horizons described). Vegetation includes Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, and various bryophytes.

### Climate and soil context (1997–2014)
- Mean air temp: 8.0 °C; mean soil temp in control plots: 7.5 °C.
- Mean annual rainfall: 1411 mm; Total N-deposition: 20–25 kg N ha-1 yr-1.
- Soil characteristics provided across horizons (C, N, C:N, base cations, H+, CEC, etc.).

### Vegetation and chemistry
- Vegetation: extensive bryophyte cover; community includes heather and associated bryophytes; litterfall and biomass values are provided for baseline years.
- Vegetation chemistry data include C, N, C:N ratios, and nutrient contents for key species and litter.

## Climate change treatment information
- Treatments: drought and warming; each with three replicated plots (4 m x 5 m) and three controls (n=9 plots total).
- Drought
  - Automated retractable polyethylene roof; operates May–Sept (1999–2011) and later Apr–Oct.
  - Reduces annual rainfall ~20%; excludes ~80% of rainfall during active period due to sensor limitations.
  - Not operated in high winds (>10 m/s); operation changes over time (2012 onward adjustments; 2016 roof rainfall accumulation issues).
- Warming
  - Retractable aluminium mesh curtains; reduce infrared radiation and conserve heat at night.
  - Roofs retract upon rainfall detection to avoid rainfall exclusion; about 14% of annual rainfall is excluded on average.
  - Limited by high winds; operation mitigated during adverse conditions.
- Maintenance and issues
  - Frames refurbished/replaced; new frames installed on top of old frames in June 2017 to minimize vegetation disturbance.
  - Rainfall sensor malfunction since Jan 2018; drought roofs off in 2016 due to refurbishments and water accumulation; COVID-19 affected field work in 2020–2021.
- Growing degree days (GDD)
  - Tabled calculations show year-by-year changes in GDD due to warming; guidance to use percent change in GDD for completeness when year data are incomplete.

## Equipment, protocols and data processing methodology
- On-site automated weather station (AWS) plus plot-level sensors (micro-met data); broad data types collected (abiotic and biotic).
- Data inventory (Table 7) includes:
  - AWS meteorological data: humidity, air temp, rainfall, pressure, net/radiation, solar radiation, PAR, wind.
  - Micro-meteorological plot data: soil/air temperature and soil moisture.
  - Rainfall: ground-level gauge and throughfall data; rain chemistry.
  - Soil/biogeochemical measurements: soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter chemistry, and root/microbial biomass.
- Data cadence and processing
  - Micro-meteorological plot data logged per minute; hourly averages (pre-2016) and half-hourly averages (post-2016).
  - AWS data sampled every minute; hourly averages produced; quality control via manual Excel-based checks.
  - Throughfall and rainfall gauges used to derive plot-level rainfall by applying percent-change adjustments to site-level rainfall; data exclusion and occasional infilling when measurements are compromised.
- Data storage and accessibility
  - Some data are not stored at EIDC or not available after June 2015; contact Sabine Reinsch or Bridget Emmett for further details.
  - Detailed protocols and sensor specifications (sensor types, brands, and methods) are documented in the dataset description.

## Micro-meteorological data – plot level data
- Continuous measurements since 2008; earlier micro-meteorological data described in the documentation.
- Soil temperatures recorded at 5, 10, and 20 cm depths using Campbell Scientific sensors.
- Soil moisture measured with TDR sensors (CS616) since 2008; earlier manual theta probe measurements used.
- Data at a minute-level resolution, with hourly or half-hourly summaries depending on the period.

## Storage rain gauge data (site level rainfall) and rainfall chemistry
- Rainfall measured with a robust ground-level storage rain gauge (12.7 cm funnel) with biweekly collection.
- Used as the primary rainfall record for site-level totals; less susceptible to logger downtime and power loss than AWS data.
- Rainfall chemistry also collected; data used in conjunction with throughfall measurements to estimate plot-level rainfall.

## Throughfall data (plot level rainfall)
- Collected biweekly using plot-level funnels and bottles; reports rainfall per plot.
- Data adjustments required to harmonize with site-level rainfall to generate seasonal/annual totals.
- Data quality flags for incomplete or compromised measurements; some plots excluded from means when data are missing or unreliable; occasional infilling with year-average reductions.

## Appendix
- Site layout figures and quadrat measurement area diagrams.

Notes for data governance and stewardship
- Data accessibility is through a public data centre (EIDC) with clear reference to the collection and data type; some data are not continuously stored at EIDC.
- Metadata completeness is strong (detailed site description, treatment specifics, sensor types, depths, units, and time scales). However, there are gaps due to sensor failures and external disruptions (e.g., broken rainfall sensor since 2018, COVID-related access restrictions).
- Data quality control relies on manual QC in addition to automated checks; documentation emphasizes context around data processing decisions (how throughfall is used to adjust site rainfall, handling of missing data, and when to exclude plots).
- The dataset is longitudinal (1997–present) with complex treatment management; researchers and data stewards should account for changes in treatment operation (e.g., drought roof timing shifts, 2016–2017 frame replacement) when using long-term time series.
- For comprehensive or updated data beyond what is stored at EIDC (especially post-2015), contact the listed researchers for access and metadata details.