# Climoor field site in Clocaenog forest. Supporting documentation for data

- An automated climate change manipulation experiment (climate drought and warming) at Climoor/Clocaenog field site, established in 1998.
- Data corpus includes micro-meteorological plot-level observations (2016–2021) and extensive site- and plot-scale climate and ecological measurements collected since 1998.
- Aimed at understanding drought and warming effects on upland moorland ecosystems, with detailed treatment histories, equipment protocols, and data processing notes to support reuse in analyses and models.

## Data access and citation

- Data available at: https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
- Licensing: Open Government Licence; users must comply with terms.
- Citation to use: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015

## Data structure

- File: clm_micromet_2016-2021_summaryqa.csv
- Contents: 28 columns; data marked NA for not recorded and -9999 for faulty data.
- Example variables (sample): 
  - Date (YYYY-MM-DD)
  - TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, …, TSoil5cm_Plot9_degC (soil temperature at 5 cm depth)
  - TSoil20cm_Plot1_degC, …, TSoil20cm_Plot9_degC (soil temperature at 20 cm depth)
  - Soil_moisture_Plot1_m3_per_m-3, …, Soil_moisture_Plot9_m3_per_m-3 (volumetric soil moisture)
- Timeframe: micro-meteorological data at plot scale from 2016–2021; data prior to 2016 are described in related documentation.
- Data handling: data quality controlled by basic QC; values encoded as NA or -9999 where appropriate.

## Site overview

- Location: Clocaenog Forest, North East Wales (53°03′19″N, 03°27′55″W).
- Ecosystem: upland west-atlantic moorland, dominated by Calluna vulgaris (heather); notable bryophyte presence.
- Climate (1997–2014 era): mean air temp ~8.0°C; mean soil temp in control plots ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha−1 yr−1.
- Soil: humo-ferric podzol with variable E and Bh horizons; horizon depth patterns and soil chemistry provided (N, C, C:N, base cations, etc.).
- Vegetation composition and biomass data available; species list includes Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, various bryophytes.

## Climate change treatments

- Design: two treatments (drought and warming) plus three replicated control plots (total 9 plots).
- Drought treatment:
  - Mechanism: retractable polyethylene roof triggered by rainfall sensor to exclude rainfall during the May–September period (1999–2011; later Apr–Oct since 2012).
  - Effect: reduces annual rainfall by ~20% (site-specific context); excludes ~80% of rainfall during drought windows due to sensor thresholds.
  - Operational challenges: roofs do not operate in high winds (>10 m s−1); issues with rainwater accumulation leading to incomplete retraction since 2016.
- Warming treatment:
  - Mechanism: retractable aluminum mesh curtains over plots during the night; reflects ~96–97% infrared radiation, reducing nighttime heat loss by ~64%.
  - Rainfall interaction: rainfall is detected and roofs retracted to prevent rainfall exclusion; time lag between detection and retraction can cause some rainfall exclusion.
- Maintenance and frame updates:
  - 2016: frames refurbished; drought/warming mechanisms periodically required more maintenance.
  - 2017: new frames installed on top of old ones to minimize vegetation disruption.
  - Post-2016: drought roofs intermittently not active due to frame refurbishments and water accumulation; COVID-19 interruptions affected field work in 2020–2021.
- Documentation of treatment details:
  - Table 5: mapping of plot numbers to treatment types (warming, drought, control).
  Table 6: year-by-year drought and warming operation details, including dates and percent rainfall reductions.
  - Growing Degree Days (GDD) data provided for warming vs. control plots; method notes and calculations are described.

## Equipment, protocols and data processing

- Automated weather station (AWS) at site plus multiple sensors within treatment plots (micro-meteorological data).
- Data categories (Table 7 summary):
  - AWS meteorological data: daily measurements of relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Micro-meteorological plot data: daily soil and air temperatures, soil moisture.
  - Rainfall and rainfall chemistry: site rainfall from a ground-level storage gauge; rainfall chemistry data.
  - Throughfall data: plot-level rainfall collected biweekly using funnels and bottles; used to derive treatment-specific rainfall differences.
  - Water table depth, soil respiration, trace gas measurements (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, soil organic carbon, soil solution chemistry, and more.
- Sampling and data frequency:
  - Sensors: measurements logged at high frequency (minutes); hourly or half-hourly averages used for processing.
  - Throughfall and rainfall: biweekly collection; data may be infilled with year-average reductions if data are missing.
- Data quality and accessibility:
  - Early data QC relied on visual inspection via spreadsheets; acknowledges potential limitations of automated QC.
  - Not all data stored in the Environmental Information Data Centre (EIDC) post-June 2015; some smaller or post-2015 datasets may be stored elsewhere or with project contacts.

## Data usage notes and caveats

- Data gaps and issues to consider:
  - Drought treatment roofs inactive at times since 2016 due to refurbishment and water accumulation; warming roofs similarly affected by rain events and mechanical lag.
  - Rainfall sensor failure (2018) and COVID-19-related interruptions (2020–2021) create gaps in rainfall and related datasets.
  - Throughfall data may be incomplete due to sampler failures (funnels, bottles, overflow) requiring exclusion or infilling by average reductions.
- Timeframe considerations:
  - The main micro-meteorological dataset covers 2016–2021; broader site datasets span 1998 onwards with various variables recorded on different schedules.
- Data provenance and lineage:
  - Data are accompanied by a structured description of instruments, sampling frequencies, and processing steps; Table 7 and Appendix figures provide context for site layout and measurement areas.
- For additional details or datasets not in EIDC:
  - Contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for access to non-EIDC data or datasets collected after June 2015.

## Tables and figures referenced in documentation

- Table 5: Climate change treatment plots (plot number → treatment type).
- Table 6: Drought and warming treatment histories, with yearly dates and reductions; includes GDD calculations (Table 6(b)).
- Table 7: Summary of data measured at the Clocaenog field site (data sources and time scales).
- Appendix figures: site layout and quadrat arrangement, measurement areas.

## Contacts

- Primary data contacts for further details or access to non-EIDC data: Sabine Reinsch and Bridget Emmett (enquiries@ceh.ac.uk).