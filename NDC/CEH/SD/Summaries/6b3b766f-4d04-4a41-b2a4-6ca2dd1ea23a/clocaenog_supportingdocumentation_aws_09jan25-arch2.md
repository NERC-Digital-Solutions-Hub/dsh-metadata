# Climoor field site in Clocaenog forest. Supporting documentation for data

## Overview
- Long-running climate change manipulation experiment at Climoor field site (Clocaenog Forest, North East Wales) begun in 1998.
- Automated drought and warming treatments designed to reflect predicted climate changes for the next 20–30 years.
- Experimental design: two treatments (drought, warming) with three replicates each plus three control plots (total n=9 plots).

## Data Access
- Data available from the Environmental Information Data Centre (EIDC): Daily automated weather station (AWS) data for Climoor field site.
- Specific dataset file: CLM_AWS_2024_summaryQA.csv (CSV; 10 columns, 367 rows).
- Data quality: missing values marked as NA; faulty data replaced by -9999.

## Data Structure
- File: CLM_AWS_2024_summaryQA.csv
- Columns (Date, Year–Month–Day) and meteorological variables:
  - Mean_air_temperature_degC
  - Minimum_air_temperature_degC
  - Maximum_air_temperature_degC
  - Rainfall_mm
  - Air_pressure_mbar
  - Solar_radiation_kW_per_m2
  - Photosynthetic_active_radiation_umol_per_m2_per_sec
  - Wind_speed_m_per_sec
  - Wind_direction_degrees

## Site Information
- Habitat: upland west-Atlantic moorland; dominant species include Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; bryophytes prominent.
- Soil: humo-ferric podzol with variable horizons (Eg, Bh); soil chemistry and structure detailed in Table 2 of the documentation.
- Climate (1997–2014): mean air temp 8.0 °C; mean soil temp in control plots 7.5 °C; mean annual rainfall 1411 mm; total N deposition 20–25 kg N ha⁻¹ yr⁻¹.
- Vegetation metrics: annual litterfall ~177 g m⁻²; biomass and cover data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, and bryophytes.

## Climate Change Treatment Information
- Treatments and design: two treatments (drought and warming) with three replicate plots each; three control plots with scaffolding to mimic shading (9 plots total).
- Drought treatment:
  - Automated retractable polyethylene roof; active May–September (and Apr–Oct since 2012).
  - Rainfall reduction: ~20% annually; up to ~80% of rain excluded due to sensor limits.
  - Operation paused in high winds (>10 m s⁻¹); frames refurbished in 2016 and new frames installed in 2017.
- Warming treatment:
  - Retractable aluminum mesh curtains; reflect infrared radiation to reduce heat loss at night.
  - Roofs retract in response to rain detection; ~14% annual rainfall reduction.
  - Rainfall exclusion due to lag in retraction; wind safety considerations.
- Operational notes:
  - Data include annual and seasonal rainfall reduction figures (Tables 6a and 6b).
  - Post-2016 frame replacement and refurbishment affected operation continuity.
  - Some years with incomplete operation or data due to refurbishment, wind, or COVID-19.

## Equipment, Protocols and Data Processing Methodology
- On-site AWS (automated weather station) and plot-level micro-meteorological sensors.
- AWS measurements:
  - Parameters: temperature (air, min, max), humidity, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction.
  - Sampling: every minute; data averaged hourly (initially) or half-hourly (after 2016).
  - QC: visual checks in Excel; no strict automated bounds used to preserve context.
- Micro-meteorological (plot-level) data:
  - Soil temperature at 5, 10, 20 cm; soil moisture (TDR sensors since 2008; earlier theta probe).
  - Data frequency: daily to hourly depending on dataset; QC similar to AWS data.
- Rainfall data and throughfall:
  - Site rainfall: ground-level rain gauge with biweekly collection.
  - Plot throughfall: funnel-and-bottle collectors; data used to derive plot-level rainfall via percent-change adjustments relative to site rainfall.
  - Data handling: plots with compromised data excluded from treatment means; occasional infilling with year-average reductions when appropriate.

## Data Storage and Access
- Primary data stored and accessed through EIDC; long-term data stewardship.
- Documentation includes data file structure, site characteristics, and treatment methods to support reuse and integration with other environmental datasets.

## Data Quality, Gaps and Limitations
- Gaps and issues:
  - Rainfall sensor on site broken since 04 Jan 2018.
  - Drought roofs not operated fully from 2016 onward due to refurbishment and water accumulation; COVID-19 restrictions affected field visits in 2020–2021.
  - Some years have incomplete measurements or unvisited periods, leading to gaps in rainfall throughfall data.
- These factors should be accounted for when combining this dataset with other data sources or performing long-term trend analyses.

## Contacts
- Primary contacts for inquiries: Sabine Reinsch and Bridget Emmett (enquiries@ceh.ac.uk).

## Notes for Analysts Monitoring the Environment
- The Climoor/Clocaenog dataset provides standardized, long-term AWS and plot-level meteorological data coupled with climate manipulation treatments.
- Useful for analyses of drought and warming effects on upland moorland ecosystems, including hydrology, soil processes, and vegetation responses.
- Data processing approach accommodates combining site rainfall with throughfall-derived adjustments to yield plot-level rainfall estimates, enabling comparisons across years and treatments.
- Consider data gaps (sensor failures, refurbishment periods, pandemic disruptions) when assessing temporal trends or integrating with external environmental datasets.