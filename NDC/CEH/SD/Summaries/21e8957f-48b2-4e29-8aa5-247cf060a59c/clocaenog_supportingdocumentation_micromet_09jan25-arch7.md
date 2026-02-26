# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1. Data access
- Data are available via the Environmental Information Data Centre (EIDC).
- Data collection: Daily plot-level (micro meteorological) data at Climoor field site in Clocaenog Forest.
- Reference: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## 2. Data structure
- Dataset: CLM_AWS_2024_summaryQA.csv
- Size: 28 columns, 367 rows
- Data quality marks: Missing values as "NA"; faulty data replaced by "-9999"
- Example variables include:
  - Date (Year-Month-Day)
  - Soil temperature at 5 cm for plots (e.g., TSoil5cm_Plot1_degC)
  - Soil temperature at 20 cm for plots (e.g., TSoil20cm_Plot1_degC)
  - Soil moisture (e.g., Soil_moisture_Plot1_m3_per_m-3)
  - Multiple plots with warming, drought, and control labels

## 3. Site information
- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W)
- Habitat: upland west-atlantic moorland; dominated by Calluna vulgaris (heather)
- Vegetation: bryophytes present; species list includes Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, etc.
- Soil: humo-ferric podzol; horizons Eg and Bh variably evident; typical horizon depths around 6–17 cm with Bh below parent material
- Climate context (1997–2014):Mean air temp ~8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; N deposition ~20–25 kg N ha⁻¹ yr⁻¹
- Site characteristics: Replicated drought and warming treatments; framed and solar/wind-powered automated systems

## 4. Climate change treatment information
- Treatments: Drought and warming, each with three replicates; three control plots (total 9 plots)
- Drought treatment:
  - Automated retractable roof over plots (4 m x 5 m)
  - Triggered by tipping-bucket rainfall sensor; May–Sept reductions ~20% annual rainfall; up to ~80% of rain excluded during active periods
  - Since 2012, timing shifted to Apr–Oct; since 2016, rainwater accumulation reduced roof retraction efficiency
- Warming treatment:
  - Retractable aluminium mesh curtains; reflect ~96–97% infrared, reducing night heat loss
  - Active during night with a light sensor; retracted if rain detected (15 minutes after darkness)
  - Average annual rainfall reduction ~14% due to retraction timing
  - Wind protection: curtains do not operate in winds > 10 m s⁻¹
- Frame refurbishment:
  - Original frames gradually failed; new frames installed on top of old ones in June 2017 to minimize vegetation disturbance
- Treatment timing and metrics (examples):
  - Year-by-year reduction in annual/growing-season rainfall (varies by year and treatment)
  - Growing degree days (GDD) calculated for control and warming plots to quantify warming effect
- Layout:
  - Plots 1–9 correspond to different treatments and replicates (W = warming, D = drought, C = control)

## 5. Equipment, protocols and data processing methodology
- On-site automated weather station (AWS) for meteorological data; plot-level sensors for micro-meteorological data
- Data categories collected (Table 7 summary):
  - AWS meteorological data: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Plot-based abiotic/biotic data: soil and air temperatures, soil moisture, rainfall throughfall, water table depth, soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution chemistry
- Data cadence and processing:
  - AWS sensors sample every minute; hourly averages (pre-2016) or half-hour averages (post-2016)
  - Micro-met data (plot-level) recorded daily; soil temperature at multiple depths (5, 10, 20 cm); soil moisture via TDR sensors (m3/m3)
  - Quality control primarily via visual inspection in spreadsheets; no automated limit scripting described
- Rainfall data:
  - Ground-level storage rain gauge (biweekly collection) preferred for reliability over AWS data
  - Throughfall collected biweekly per plot with a funnel and bottle; data used to compute plot-level rainfall changes relative to site rainfall
- Appendices:
  - Site layout and quadrat arrangement (plots, motor box, measurement areas)

## 6. Data streams and spatial context (GIS-ready considerations)
- Spatial design:
  - Nine 4 m x 5 m plots arranged as warming, drought, and control treatments across three replicates
  - Plot-level sensors enable map-based visualization of treatment effects over time
- Data types suitable for GIS:
  - Plot-level treatment maps (W/D/C per plot)
  - AWS meteorological layers (daily/hourly rainfall, temperature, radiation, humidity)
  - Soil temperature/moisture profiles by depth (5, 10, 20 cm)
  - Rainfall throughfall and canopy/vegetation data for ecosystem modelling
  - Vegetation composition, litterfall, and canopy reflectance datasets for overlay with climate manipulation
- Metadata and provenance:
  - Clear documentation of data sources, sensor types, time scales, and processing steps
  - Note on data where storage or collection locations vary (EIDC vs. other storage post-2015)

## 7. Data quality, limitations and considerations for use
- Data quality notes:
  - Missing values coded as NA; faulty readings replaced by -9999
  - Rainfall sensor on-site broken since 04 Jan 2018; gap implications for site rainfall estimates
- Operational limitations:
  - Drought roofs sometimes miss smaller rain events due to sensor limits; roof operation suspended during high winds (>10 m s⁻¹)
  - Post-2016 refurbishment and rainwater accumulation affecting drought roof retraction
  - COVID-19 restrictions affected field visits in 2020–2021, impacting data collection
- Data availability caveats:
  - Some datasets stored outside EIDC after June 2015; contact CEH colleagues for details
  - GDD calculations and warming assessments rely on plot-scale meteorological data, with gaps in some years
- Guidance for GIS work:
  - When building time-series maps, account for missing years and sensor outages
  - Apply rainfall adjustments using throughfall vs. site rainfall to estimate plot-level precipitation
  - Use GDD-based indicators to quantify warming effects alongside direct temperature measurements