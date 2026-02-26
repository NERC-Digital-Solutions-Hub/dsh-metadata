# Climoor field site in Clocaenog forest. Supporting documentation for data

## Access, licensing and citation
- Data available at https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
- License: Open Government Licence
- Please cite: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979

## Data structure
- Single dataset: CLM_AWS_2016-2021_summaryQA.csv
- 10 columns; values not recorded marked NA; faulty data replaced by -9999

## Site information
- Location: Clocaenog Forest, North East Wales, UK (upland moorland habitat)
- Dominant vegetation: Calluna vulgaris (heather) with Vaccinium myrtillus, Empetrum nigrum and others
- Soil: humo-ferric podzol with variable horizons (Eg, Bh, etc.); detailed soil chemical characteristics provided
- Ecosystem and vegetation: typical upland west-atlantic moorland; annual litterfall ~177 g m^-2; bryophyte-rich understory
- Climate (1997–2014 overview): mean air temperature ~8.0°C; mean soil temperature in control ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha^-1 yr^-1
- Additional site data available in Table 2 (soil properties) and Table 3 (vegetation cover/biomass)

## Climate change treatment information
- Treatments: drought and warming, each with three replicate plots plus three control plots (total n=9)
- Drought treatment
  - Mechanism: retractable polyethylene roof triggered by rainfall sensor; aims to reduce growing-season rainfall
  - Timing: May–Sept originally; since 2012, Apr–Oct
  - Effect: ~20% reduction in annual rainfall; up to ~80% reduction of rainfall during active drought periods due to sensor thresholds
  - Operational notes: roofs do not operate in winds >10 m s^-1; roof failures and maintenance issues led to frame replacement in 2017
- Warming treatment
  - Mechanism: retractable aluminium mesh curtains to reduce night-time heat loss; reflects ~96–97% of infrared radiation
  - Activation: roof operates after ~15 minutes of darkness; rain triggers retraction to mitigate rainfall loss
  - Effects: approximate annual rainfall reduction ~14% due to retraction lag
  - Operational notes: similar wind-limit safety; refurbishments in 2016–2017 and frame replacement in 2017
- Documentation of treatment timing and annual rainfall reductions is summarized in Table 6a (Drought) and Table 6b (Warming), including years with incomplete data or equipment issues (e.g., sensor failures, COVID-related disruptions)

## Equipment, protocols and data processing methodology
- Data collection infrastructure
  - Automated Weather Station (AWS) on site for meteorological data (daily to current day)
  - Micro-meteorological (plot-scale) sensors for soil/air temperature and soil moisture
  - Rainfall measurements via a ground-level storage rain gauge and throughfall collectors per plot
  - Additional datasets: soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, vegetation surveys, canopy reflectance, phenology, litter chemistry, root and microbial biomass, and soil properties
- Data types and frequency
  - AWS meteorological data: measured with minute-level resolution; hourly averages maintained
  - Micro-met data: plot-level measurements since 1998, with daily sampling initially; post-2016 logged as half-hourly or hourly averages
  - Rainfall data: biweekly storage gauge data preferred for robustness; throughfall collected per plot and used to derive plot-level rainfall by applying percent differences to site-level rainfall
  - Data quality control: primarily visual checks in Excel to identify trends and anomalies
- Data processing notes
  - Dissipation of missing data (NA) and questionable data (-9999) handling described
  - Throughfall processing involves excluding plots with compromised data; imputation by year-average reductions used rarely
- Data storage and access notes
  - Not all data are stored in the Environmental Information Data Centre (EIDC); contact the authors for full data details
  - Inquiries: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)

## Data availability and contact points
- Primary AWS data and ancillary measurements are described; some datasets post-2015 are not fully stored at EIDC
- For additional details or access to non-EIDC datasets, contact Sabine Reinsch or Bridget Emmett

## Appendix and figures
- Appendix includes site layout figures and quadrat arrangement (0.5 m^2 quadrats) for context and measurement areas
- Figure references illustrate frame changes and rainfall/throughfall measurement setup