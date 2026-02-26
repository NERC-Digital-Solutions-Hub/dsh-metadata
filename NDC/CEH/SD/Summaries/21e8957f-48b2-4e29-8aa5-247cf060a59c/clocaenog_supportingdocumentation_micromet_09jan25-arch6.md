# Climoor field site in Clocaenog forest. Supporting documentation for data

## Data access
- Data available from the Environmental Information Data Centre (EIDC) under the collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest. URL: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## Data structure
- Dataset: CLM_AWS_2024_summaryQA.csv
- Size: 28 columns, 367 rows
- Data quality marks: "NA" for not recorded; "-9999" for faulty data
- Content overview:
  - Daily date field (Year-Month-Day)
  - Soil temperature: TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, TSoil5cm_Plot3/Plot4_degC, etc. (5 cm depth; by plot)
  - Soil temperature at 20 cm: TSoil20cm_PlotN_degC
  - Soil moisture: Soil_moisture_PlotN_m3_per_m3
  - Descriptions indicate warming vs. control plots and plot numbers
- Note: Dataset represents a snapshot of plot-level measurements; not all variables are stored in the same repository over time.

## Site information
- Purpose: Climate change manipulation experiment (since 1998) at Clocaenog Forest, upland moorland, using automated roof technology to simulate drought and warming
- Target habitat: Upland moorland with Calluna vulgaris as dominant taxa
- Location: Clocaenog Forest, North East Wales; coordinates provided; site designed for solar/wind power
- Treatments: Replicated drought and warming treatments with controls (3 replicates per treatment; 9 plots total)
- Vegetation and soil: Heather-dominated shrub layer; bryophytes present; humo-ferric podzol soil with horizon structure described

## Climate change site characteristics (3.1)
- Climate (1997–2014):
  - Mean air temperature: ~8.0°C
  - Mean soil temperature in control plots: ~7.5°C
  - Mean annual rainfall: ~1411 mm
  - Total nitrogen deposition: 20–25 kg N ha−1 yr−1
- Soil: Humo-ferric podzol; horizons and soil chemistry metrics (N, C, C:N, base cations, H, Al, CEC, base saturation) detailed by horizon
- Vegetation: Dominant species include Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; bryophyte coverage high; annual litterfall ~177 g m−2
- Vegetation chemistry: Elemental contents (C, N) and ratios (C:N) reported by species and litter
- Appendix visuals: Site layout and quadrat arrangement

## Climate change treatments (4)
- Structure: Two treatments (drought and warming) with three replicate plots each and three control plots
- Drought treatment:
  - Operation: Retractable polyethylene roof; triggered by tipping-bucket rainfall sensor
  - Rainfall reduction: ~20% annual; up to ~80% of rainfall excluded during drought period
  - Schedule: Primarily May–September (1999–2011), extended to April–October from 2012; affected by rainwater accumulation on roofs since 2016
- Warming treatment:
  - Operation: Retractable aluminium mesh curtains; reflect 96–97% infrared radiation
  - Rain interaction: Curtains retracted when rain detected to minimize rain exclusion; typical annual rainfall reduction ~14%
  - Operation window: Night-time warming with a 15-minute dark interval; rain-triggered retraction
- Operational notes:
  - Winds >10 m s−1 limit curtain operation
  - Mechanical frame refurbishments occurred in 2016–2017; new frames installed June 2017
  - Table 6 provides year-by-year drought and warming details, including rainfall reductions and operational notes
  - GDD (Growing Degree Days) calculations provided for warming vs. control; year-by-year changes documented
- Data interpretation guidance: GDD changes are computed from plot-scale air temperature data; percent changes recommended when year-round data are incomplete

## Equipment, protocols and data processing methodology (5)
- Data collection infrastructure:
  - Automated Weather Station (AWS) for meteorological data
  - Plot-level micro-meteorological sensors
  - Abiotic and biotic data streams across plots
- Data catalog (Table 7):
  - AWS meteorological data: RH, air temperature, rainfall, pressure, net radiation, solar radiation, PAR, wind
  - Micro-meteorological plot data: soil/air temperature and soil moisture
  - Rainfall and rainfall chemistry: ground-level gauge and rain collectors
  - Throughfall data: plot-level rainfall
  - Water table depth, soil respiration, trace gas fluxes (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter chemistry
  - Vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution chemistry
  - Note: Not all data stored in EIDC after June 2015; contact CEH staff for details
- Micro-meteorological data (5.1):
  - Sensors measure soil temperature at multiple depths (5, 10, 20 cm) and soil moisture (TDR CS616)
  - Data frequency: minute-level measurements; hourly averages until Jan 2016; half-hourly averages thereafter
  - Data quality control: simple visual QC in Excel; alternative automated QC not applied due to contextual memory of conditions
- Rain gauge data (5.2):
  - Site rainfall: storage rain gauge (biweekly collection), robust to logger outages
  - Rainfall chemistry: monthly measurements
- Throughfall data (5.3):
  - Plot-level rainfall captured biweekly using funnels and bottles
  - Data processing: convert to annual/seasonal rainfall by applying plot-level reductions to site rainfall; data gaps lead to exclusion of some plots from means; infilling used only when necessary
- Appendix materials:
  - Site layout figures and quadrat mapping illustrate measurement areas and plot arrangement

## Data quality, gaps, and cautionary notes
- Data gaps and issues:
  - Drought roofing operations affected by rainfall patterns and, since 2016, by water accumulation
  - Rainfall sensor on site broken since 2018
  - Some years have incomplete data or require infilling; not all data stored in EIDC after mid-2015
  - Throughfall data can be compromised by equipment loss (funnels, bottles) or overflow; treatment means may be computed with fewer than three replicates
- User guidance:
  - For GDD and warming analyses, use year-by-year percent changes when data completeness is variable
  - Contact authors or CEH Bangor for datasets not stored in EIDC or for clarifications on data processing steps