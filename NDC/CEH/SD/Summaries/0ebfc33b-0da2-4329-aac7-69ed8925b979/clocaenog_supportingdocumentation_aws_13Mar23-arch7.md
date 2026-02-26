# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access and citation
- Data are accessible at: https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- License: Open Government Licence
- Recommended citation: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979

## Data structure
- File: CLM_AWS_2016-2021_summaryQA.csv
- Columns (10): Date (Year-Month-Day), Mean_air_temperature_degC, Minimum_air_temperature_degC, Maximum_air_temperature_degC, Rainfall_mm, Air_pressure_mbar, Solar_radiation_kW_per_m2, Photosynthetic_active_radiation_umol_per_m2_per_sec, Wind_speed_m_per_sec, Wind_direction_degrees
- Data quality marks: NA = not recorded; -9999 = faulty data
- Date format: Year-Month-Day

## Site information
- Automated climate manipulation site established in 1998 in Clocaenog Forest, North East Wales
- Treatments: replicated drought and warming schemes (3 replicates each) plus 3 control plots
- Location: upland west-Atlantic moorland; dominant vegetation includes Calluna vulgaris (heather) and bryophytes; surrounding flora listed
- Soil: humo-ferric podzol with variable horizons (including Eg and Bh); soil properties summarized in tables
- Growing season: June–August; shoulder seasons April–May and September–October; winter dormancy
- Climate and soil context (1997–2014): mean air temp ~8.0°C; mean soil temp control ~7.5°C; mean annual rainfall ~1411 mm; N deposition ~20–25 kg N ha-1 yr-1

## Climate change site characteristics
- Vegetation and biomass data indicate dominance of Calluna vulgaris with bryophytes; annual litterfall ~177 g m-2
- Soil characteristics (horizons LF, Oh, Eg, Bh) with nutrient and CEC values provided; CEC ranges by horizon
- Environment typology: Wet upland heath; typical soil and horizon properties described

## Climate change treatment information
- Treatments: drought and warming, each with 3 replicate plots; 3 controls (total 9 plots)
- Treatment layout: tabled plot-to-treatment mapping (Table 5)
- Drought treatment
  - Operation: May–September (1999–2011); extended May–Oct since 2012
  - Mechanism: retractable polyethylene roof activated by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% (and up to ~80% of rain during detectable events)
  - Constraints: roofs do not operate in winds >10 m s-1; post-2016 rainwater accumulation caused operation issues; frames refurbished in 2016–2017 with new frames installed mid-2017
- Warming treatment
  - Mechanism: retractable aluminium mesh curtains over plots during night; reflect 96–97% of infrared radiation; reduces night heat loss
  - Activation: triggered by a light sensor with a 15-minute dark threshold
  - Rainfall interaction: tipping-bucket sensor retracts roofs on rain to mitigate rainfall exclusion; overall ~14% annual rainfall reduction
  - Operational notes: wind limits; some years missing data due to frame changes and COVID-related disruptions (2016 refurbishment; 2017 new frames)
- Frame and maintenance notes
  - 2016 refurbishment due to frame aging; 2017 new frames installed atop old ones to minimize vegetation disturbance
- Year-by-year treatment details
  - Table 6(a): drought treatment dates and percent rainfall reductions (1997–2011, with later years showing ongoing variation and gaps)
  - Table 6(b): warming treatment Growing Degree Days (GDD) and percent changes by year; notes on years with NA or special conditions
  - GDD calculations use plot-level air temperature measures; indicates warming effects over time

## Equipment, protocols and data processing methodology
- Equipment and data types
  - Automated Weather Station (AWS) for meteorological data (daily to current-day daily averages)
  - Micro-meteorological (plot-level) sensors for soil/air temperature and soil moisture
  - Rainfall measurements: ground-level storage rain gauge (biweekly); plot-level throughfall collectors (biweekly)
  - Additional datasets: soil respiration, trace gases, canopy reflectance, vegetation surveys, litterfall, root biomass, soil chemistry, etc. (not all stored in EIDC)
- Data collection and quality control
  - AWS sensors measure at 1-minute intervals; hourly averages used for QC
  - Micro-met data collected since 1998–present; post-2016 data logged as half-hourly averages or daily averages
  - Data quality control primarily via manual Excel-based visual checks
- Rain data specifics
  - Site rainfall (storage gauge) is preferred for robustness; throughfall data used to compute plots’ rainfall as a percent change relative to site rainfall
  - Plot-level data can be incomplete if collectors fail or data are lost; infilling used sparingly with average reductions when necessary
- Data availability notes
  - Not all datasets stored in the EIDC; some post-June 2015 data are not included; contact project researchers for details

## GIS-relevant considerations for using the data
- Spatial components
  - Plot layout and quadrat mapping provided (appendix figures illustrating quadrat and motor box layout)
  - Precise site coordinates and plot arrangement enable GIS-based visualization of treatments
- Temporal coverage and gaps
  - AWS data: 2016–2021
  - Drought and warming treatment details span 1997–2021 with gaps due to refurbishment, instrumentation issues, and COVID-19
- Data quality and completeness
  - Some years have incomplete rainfall data (sensor issues, broken rainfall sensor since 2018)
  - Throughfall and other plot-level data may have incomplete weeks or replicates in certain years
- Data licensing and citation
  - Data are openly licenced under the Open Government Licence; cite Reinsch et al. (2022) when using the dataset
- Practical GIS use
  - Use the CLM_AWS_2016-2021_summaryQA.csv to map weather variables across time
  - Integrate with plot-level treatment maps to analyze spatial patterns of drought and warming effects
  - Combine with vegetation and soil data to assess habitat responses under climate manipulations
  - Consider data gaps and sensor downtime when performing time-series analyses or generating annual summaries