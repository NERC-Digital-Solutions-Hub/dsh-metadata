# Climoor field site in Clocaenog forest. Supporting documentation for data

- A climate change manipulation experiment (Climoor/Clocaenog field site) established in 1998 using automated roof technology to create drought and warming treatments reflecting predicted climate changes over the next 20–30 years.
- Author and version: Sabine Reinsch; Micromet version dated 24 Jan 2024.

## Data access

- Data available from Environmental Information Data Centre (EIDC).
- Data collection focus: Daily plot-level micro-meteorological data at Climoor field site in Clocaenog Forest.
- Access link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## Data structure

- Core dataset: CLM_AWS_2022-2023_summaryQA.csv
  - 28 columns, 731 rows
  - Date format: Year-Month-Day
  - Includes: Soil temperature at 5 cm and 20 cm (per plot), soil moisture per plot, and other meteorological/abiotic data
  - Data quality flags: "NA" for missing data; "-9999" for faulty data

## Site information

- Location and habitat
  - Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W)
  - Upland moorland habitat dominated by Calluna vulgaris (heather) >60% of plant biomass
  - Plant species present include Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes, and others
- Soil
  - Humo-ferric podzol; soil horizons Eg and Bh may be variably visible
  - Depths and characteristics provided (N, C, C:N, base cations, etc.)
- Climate (1997–2014)
  - Mean air temperature: 8.0 °C
  - Mean soil temperature in control plots: 7.5 °C
  - Mean annual rainfall: 1411 mm
  - Total N deposition: 20–25 kg N ha-1 yr-1
- Vegetation and chemistry
  - Detailed vegetation cover/biomass data at experiment start (1998) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
  - Vegetation chemistry and related metrics (C, N, C:N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) by species and litter

## Climate change treatments

- Experimental design
  - Two treatments: drought and warming
  - Each treatment replicated in three plots; three additional control plots
  - Total plots: 9 (4 m x 5 m each)
  - Drought and warming frames evolved over time; scaffolding and automatic mechanisms updated in 2017
- Drought treatment
  - Year-round operation May–Sept (1999–2011); extended Apr–Oct since 2012
  - Mechanism: Retractable polyethylene roof over plots to reduce rainfall by ~20%
  - Rainfall sensor controls roof; some rain events missed due to sensor limits
  - 2016 changes: roof operation issues; new frames installed June 2017 to minimize vegetation disturbance
  - Additional note: rainfall pattern changes and water accumulation on roofs affected operation post-2016
- Warming treatment
  - Night-time warming via retractable aluminum mesh curtains; reflects 96–97% infrared radiation, reducing night heat loss
  - Roofs retracted when rain detected to prevent rainfall exclusion; delay between rain event and roof retraction
  - Approximate annual rainfall reduction ~14%
  - Operation controlled by light sensors and rain-detection; wind limits (>10 m s-1) prevent curtain operation
- Operational notes
  - In 2017–2019, some years had partial operation due to frame refurbishment and weather
  - Rainfall sensor on site broken since 2018-01-04
  - Data tables (Tables 6a–6b) summarize year-by-year drought and warming conditions, including growing degree days (GDD) and percent changes

## Equipment, protocols and data processing

- Data collection infrastructure
  - Automated Weather Station (AWS) for meteorological data (on-site)
  - Micro-meteorological sensors within treatment plots (plot-scale data)
  - Range of abiotic and biotic measurements collected at the plots
- Data types and sampling
  - AWS: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction; daily measurements since 1999
  - Micro-met plot data: soil/air temperature and soil moisture; daily data since 1998
  - Rainfall data: site-level storage rain gauge (biweekly), plot-level throughfall (biweekly)
  - Additional data: soil respiration, trace gas measurements, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, litter, root biomass, microbial biomass, N mineralisation, SOM/SOC, soil solution
- Data formatting and QC
  - Sensor data logged as minute-level measurements; hourly averages (pre-2016) and half-hour averages (post-2016)
  - Basic QC performed visually in Excel; acknowledges limitations of automated QC limits
- Data accessibility notes
  - Not all data are stored with EIDC (some infrequent or post-June 2015 datasets may be held elsewhere)
  - Contact Sabine Reinsch or Bridget Emmett for details on non-EIDC datasets

## Data management considerations for GIS use

- Geospatial relevance
  - Plot-level, plot layout, and quadrat configurations described; Appendix provides site layout and quadrat mapping
  - Data are suitable for integrating with GIS for visualizing treatment areas, sensor locations, and plot-specific measurements
- Data completeness and quality
  - Some years/datastreams have gaps due to sensor failures, refurbishment, or access restrictions (e.g., COVID-19, 2018 rain sensor issue)
  - Throughfall and rainfall data require processing to produce plot-level rainfall estimates by applying percent changes to site rainfall; some plots may be excluded when data are missing
- Data integration tips
  - Use the CLM_AWS_2022-2023_summaryQA.csv as a core reference for plot-level micro-meteorology
  - Link climate treatment metadata (drought/warming, plot IDs, treatment status, timing) to sensor data for spatially explicit analyses
  - Leverage site-coordinates and the detailed site layout appendix to map treatment plots and measurement areas in GIS

## Access and contacts

- Data held at the Environmental Information Data Centre (EIDC); primary data access link provided above
- For datasets not stored in EIDC or for more details on historical/infrequent data, contact:
  - Sabine Reinsch
  - Bridget Emmett (enquiries@ceh.ac.uk)

## Summary of potential GIS applications

- Build GIS layers for:
  - Treatment plots (drought, warming, controls) and their spatial arrangement
  - Sensor locations (AWS and micro-meteorological plot sensors)
  - Throughfall collectors and rain gauges
  - Vegetation plots and quadrats
- Create time-series visualizations by plot, treatment, and data type (soil temperature at 5 cm/20 cm, soil moisture, rainfall, etc.)
- Compare climate treatment impacts using derived GIS attributes (e.g., drought reduction percentage, warming percentage, GDD changes)
- Integrate with soil and vegetation maps to explore spatial relationships between microclimate manipulations and ecosystem responses