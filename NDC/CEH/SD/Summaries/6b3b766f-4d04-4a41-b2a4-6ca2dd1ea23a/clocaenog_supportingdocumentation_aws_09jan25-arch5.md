# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access
- Data available from the Environmental Information Data Centre (EIDC) under: Data collection: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- URL: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

## Data structure
- Dataset file: CLM_AWS_2024_summaryQA.csv
- Characteristics: 1 spreadsheet, 10 columns, 367 rows
- Missing data: 'NA' indicates not recorded; faulty data replaced by '-9999'
- Columns and units (example):
  - Date (Year-Month-Day)
  - Mean_air_temperature_degC (°C)
  - Minimum_air_temperature_degC (°C)
  - Maximum_air_temperature_degC (°C)
  - Rainfall_mm (mm)
  - Air_pressure_mbar (mbar)
  - Solar_radiation_kW_per_m2 (kW m^-2)
  - Photosynthetic active radiation_umol_per_m2_per_sec (µmol m^-2 s^-1)
  - Wind_speed_m_per_sec (m s^-1)
  - Wind_direction_degrees (degrees)

## Site information
- Location and purpose: Clocaenog Forest, North East Wales (53°03'19"N, -03°27'55"W). Automated climate manipulation site established in 1998; upland moorland habitat, powered by solar and wind.
- Ecosystem and vegetation: Typical upland west-Atlantic moorland; dominated by Calluna vulgaris (heather) >60% biomass; bryophyte presence indicated with asterisks.
- Soil: Humo-ferric podzol; variable horizons (Eg, Bh); depth example 6–17 cm for Eg; parent material Ordovician/Silurian shale or mudstone.
- Climate data (1997–2014): Mean air temp ~8.0 °C; mean soil temp in control plots ~7.5 °C; mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha^-1 yr^-1.
- Vegetation metrics: Annual litterfall ~177 g m^-2; plant biomass and species cover data provided for 1998 baseline.
- Chemistry and vegetation dimensions: Tables include C, N, C:N ratios, and macronutrient content for dominant species and litter; bryophyte representation noted.

## Climate change treatment information
- Experimental design: Two treatments (drought and warming), each with three replicate plots, plus three control plots (total n=9). Treatments are 4 m x 5 m plots with scaffolding to mirror shading in controls.
- Drought treatment
  - Timing: Annually May–Sept (1999–2011); since 2012, Apr–Oct; 2016 onward affected by rainfall patterns.
  - Mechanism: Retractable polyethylene roof triggered by tipping-bucket rainfall sensor; roof excludes rainfall to reduce annual rainfall by ~20% (site is very wet); some small events missed due to sensor limits (approx. 80% of rain excluded during drought period).
  - Operational issues: 2016 onwards, accumulation of water on roof prevented full retraction; 2016 refurbishment led to the decision to install new frames on top of old frames in 2017 to minimize vegetation disturbance.
  - Data notes: Rainfall reductions are year-specific (see Table 6a); some years show operation off or partial operation due to frame issues.
- Warming treatment
  - Mechanism: Retractable aluminum mesh curtains over plots at night; reflects 96–97% of IR radiation, reducing nocturnal heat loss by ~64%.
  - Rainfall interaction: Curtains retract during rain detected by a tipping-bucket sensor after a 15-minute dark period; some rainfall is excluded due to lag between rain event and retraction.
  - Operational constraints: Curtains do not operate in high winds (>10 m s^-1) to protect equipment.
  - Data notes: Rainfall reductions ~14% annually on average; warming and drought roofs may operate together or independently (Table 6b provides year-by-year GDD comparisons and operational notes).
- Frame and equipment updates
  - 2016: Frame refurbishment; decision to install new frames on top of old frames in 2017 to minimize disruption.
  - 2017: New frame installation completed.
  - 2018 onward: Rainfall sensor on site broken since Jan 2018; drought roofs not operated from 2016 onward due to refurbishments and water accumulation; COVID-19 impacted field work in 2020–2021.
- Data interpretation guidance
  - Growing Degree Days (GDD) calculated for control and warming plots; percentage change in GDD used when year-round data completeness is variable.
  - Tables 6a and 6b provide annual drought and warming treatment specifics, including dates, percent rainfall reductions, and GDD changes.

## Equipment, protocols and data processing methodology
- Automated weather station (AWS)
  - Purpose: Provides meteorological data for on-site climate context.
  - Measurements: Relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed and direction.
  - Sampling: 1-minute measurements, aggregated to hourly averages for QA and sharing.
  - QA: Visual quality checks using basic Excel tools; preference for human interpretation over rigid automated limits to capture atypical conditions.
- Micro-meteorological (plot-scale) data
  - Plot-level sensors: Soil and air temperature, soil moisture (TDR CS616 since 2008), with earlier manual theta probes.
  - Sampling: 1-minute data; hourly (pre-2016) or half-hourly averages (post-2016).
  - QA: Similar spreadsheet-based visual checks; documented in data records.
- Rainfall data (site-level and plot-level)
  - Site rainfall: Collected with a storage rain gauge (funnel 12.7 cm diameter) and integrated approximately biweekly; preferred over AWS data due to robustness against logger power issues.
  - Plot-level rainfall: Throughfall data collected biweekly using funnels and 3000 mL bottles; data require adjustment to annual/seasonal rainfall figures.
  - Data processing: Throughfall percent changes applied to site rainfall to estimate plot-level rainfall; data gaps or contaminated measurements (e.g., funnel detachment, bottle overflow) result in exclusion of affected plots from treatment means; occasional infill with average reductions across years.
- Data storage and accessibility
  - Not all data are stored within EIDC (especially infrequent datasets or post-June 2015 data); contact researchers for details (Sabine Reinsch or Bridget Emmett).
- Metadata and documentation
  - Comprehensive site and treatment metadata provided (locations, species, soils, treatment design, frame changes, and operational notes) to support data provenance and reuse.

## Appendix and figures
- Figures referenced include site layout and quadrat arrangement, illustrating measurement areas and equipment setup.

Note: This summary emphasizes data access, structure, governance considerations, treatment metadata, data quality practices, and known data gaps—key areas relevant to Data Stewards managing climate manipulation field datasets.