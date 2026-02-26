# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access
- Data hosted by Environmental Information Data Centre (EIDC).
- Data collection: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- Access link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99
- Dataset referenced: CLM_AWS_2022-2023_summaryQA.csv (10 columns, 731 rows; NA for missing values; -9999 for faulty data).

## Data structure
- File: CLM_AWS_2022-2023_summaryQA.csv
- Columns (Example): Date (Year-Month-Day), Mean_air_temperature_degC, Minimum_air_temperature_degC, Maximum_air_temperature_degC, Rainfall_mm, Air_pressure_mbar, Solar_radiation_kW_per_m2, Photosynthetic_active_radiation_umol_per_m2_per_sec, Wind_speed_m_per_sec, Wind_direction_degrees.
- Data treatment: Missing data marked NA; faulty data replaced by -9999.

## Site information
- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W).
- Habitat: upland moorland dominated by Calluna vulgaris (heather); bryophytes present.
- Climate (1997–2014): Mean air temp ~8.0°C; Mean soil temp in control ~7.5°C; Mean annual rainfall ~1411 mm; Total N-deposition ~20–25 kg N ha^-1 yr^-1.
- Soil: humo-ferric podzol with variable horizons (Eg, Bh); typical depths around 6–17 cm for E horizon; parent material Ordovician/Silurian shale or mudstone.
- Vegetation metrics (1998 baseline): shrub cover with Calluna vulgaris (~98%), Vaccinium myrtillus (~66%), Empetrum nigrum (~25%); bryophyte cover ~73%; annual litterfall ~177 g m^-2.
- Vegetation chemistry: C, N, C:N ratios and nutrient contents reported for dominant species and litter.

## Climate change treatment information
- Treatments: two manipulated factors—drought and warming; each with three replicated plots plus three control plots (total n=9 plots).
- Drought treatment:
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor to reduce rainfall.
  - Timing: typically May–September (1999–2011); extended to April–October since 2012.
  - Rainfall reduction: about 20% annual; some small events missed by sensor; up to ~80% of rain excluded during drought periods.
  - Operational notes: roofs not used in high winds (>10 m s^-1); 2016 refurbishment led to frame replacement in 2017.
- Warming treatment:
  - Mechanism: retractable aluminum mesh curtains over plots during night; reflective to infrared radiation (96–97%); reduces night-time heat loss.
  - Operation: triggered after ~15 minutes of darkness; retracted upon detected rain to maintain rainfall input.
  - Rainfall reduction: about 14% annually; note lag between rain detection and roof retraction can exclude some rainfall.
  - Wind constraint: curtains not operated in high winds.
- Frame issues and updates:
  - By 2016 frames were aging; 2017 replacement involved placing new frames on top of old ones to minimize vegetation disruption.
- Table 6 highlights:
  - A comprehensive year-by-year summary of drought and warming treatment timings and percent rainfall reductions (1997–2023; includes notes on data gaps due to refurbishments, COVID-19, and sensor issues).
- GDD (Growing Degree Days):
  - GDD calculated for control and warming plots; percent change used to compare warming impact across years with incomplete data.

## Equipment, protocols and data processing methodology
- On-site data collection:
  - Automated Weather Station (AWS) and plot-level micro-meteorological sensors.
  - Range of abiotic and biotic data collected; summary in Table 7.
- Data sources and measurements:
  - AWS meteorological data: RH, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Micro-meteorological plot data: soil and air temperature, soil moisture (TDR), daily updates; soil temperature at multiple depths.
  - Rainfall: ground-level rain gauge (biweekly storage) preferred for robustness; throughfall data collected biweekly per plot.
  - Additional datasets: soil respiration, trace gas (CH4, N2O), net ecosystem CO2 exchange, canopy reflectance, vegetation surveys, litterfall, root biomass, microbial biomass, nutrient mineralisation, soil organic matter, soil solution chemistry.
- Data processing and QA:
  - Data quality control primarily via visual inspection in Excel; no automated enforcement limits described.
  - Some datasets stored outside EIDC, with details and access via enquiries to the listed CEH contacts.
- Data accessibility:
  - Not all datasets stored at EIDC; some are infrequently collected or post-June 2015 data.
  - For detailed datasets beyond the AWS file, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk).
- Appendix and figures:
  - Appendix includes site layout and quadrat arrangement, illustrating measurement areas.

## Data quality considerations and notable challenges
- Sensor and equipment issues:
  - Rainfall sensor malfunction since 2018; drought roofs sometimes non-operational due to frame refurbishments and water accumulation (2016–2017 onward).
  - COVID-19 disruptions impacted field visits in 2020–2021, affecting data collection windows.
- Data gaps and handling:
  - Throughfall and rainfall-related data gaps may lead to exclusion of some plots from treatment means; occasional infilling with average reductions used in long-term analyses.
  - Some years have NA or unavailable data for GDD or other metrics due to incomplete measurements.
- Data integration potential:
  - Rich multi-source dataset (AWS, micro-met, canopy, soil, litter, gas fluxes) suitable for cross-dataset environmental health assessments and policy-performance monitoring when harmonized.

## Key takeaways for environmental analysis
- The Climoor/Clocaenog field site provides a long-running, replicated climate manipulation experiment with both drought and warming treatments and robust canopy, soil, and atmospheric measurements.
- Primary data asset available for environmental health monitoring is the CLM_AWS_2022-2023_summaryQA.csv, plus extensive supplementary datasets and metadata (plants, soils, chemistry, respiration, fluxes).
- Data are accessible through the CEH EIDC, with additional datasets available via direct contact; documentation emphasizes data provenance, measurement methods, and treatment timelines.
- Analysts can assess environmental responses to drought and warming using standardized, replicated plots, though must account for gaps due to sensor issues, frame refurbishments, and COVID-related interruptions.
- For comprehensive analyses, integration with site-level rainfall, throughfall, AWS, and plot-level micro-meteorological data is possible, with attention to data quality flags and treatment-specific corrections.