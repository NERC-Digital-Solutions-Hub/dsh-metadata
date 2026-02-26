# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Automated climate manipulation experiment at Clocaenog Forest, North East Wales, established 1998.
- Reflects potential future climate: drought and warming treatments on upland moorland (heather-dominated).
- Experimental design: 9 plots (3 warming, 3 drought, 3 control) arranged in blocks; replicates allow comparison across treatments.
- Drought treatment reduces site rainfall using retractable roofs; warming treatment uses night-time aluminum curtains; both designed to operate in remote, solar/wind powered conditions.
- Site characteristics include typical upland heath vegetation (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum) and humo-ferric podzol soil.

## Data types and scope
- AWS meteorological data (on-site weather station) and micro-meteorological plot data.
- Rainfall data: storage rain gauge (site level) and rainfall chemistry; throughfall data per plot.
- Soil and hydrology: water table depth, soil respiration, trace gases (CH4 and N2O), net ecosystem CO2 exchange (NEE), and photosynthesis.
- Vegetation and biogeochemistry: vegetation survey (plant biomass via pin-point method), canopy reflectance, vegetation phenology, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, soil organic matter (SOM), soil organic carbon (SOC), bulk density, soil solution and leachate chemistry.
- Time span: data collected from 1997–2014 (with various datasets having different start dates); ongoing data handling noted up to 2015+ for some datasets.
- Some datasets are not fully stored in the central EIDC repository; contact CEH Bangor for details.

## Experimental design and climate treatments
- Treatments and replication:
  - Warming: 3 replicate warming plots.
  - Drought: 3 replicate drought plots.
  - Control: 3 control plots with scaffolding to mirror shading effects of treatments.
  - Total: 9 plots, organized in 3 blocks.
- Drought treatment specifics:
  - Historically May–September drought (1999–2011), modeled after 1995 UK drought; since 2012, runs April–October.
  - Mechanism: retractable polyethylene roof over a 4 m × 5 m plot; rainfall exclusion varies with rainfall intensity; average annual rainfall reduction ~20%, growing season reduction up to ~80% in some years.
  - Curtains inactive in winds >10 m/s to protect equipment.
- Warming treatment specifics:
  - Night-time aluminum mesh curtains reflecting infrared radiation to conserve heat; retraction occurs upon rainfall detection to preserve rainfall; average annual rainfall reduction ~14%.
  - Operation governed by light sensors and wind limits similar to drought treatment.
- Climate data recording includes detailed year-by-year tables of drought and warming timing, rainfall reductions, and GDD (growing degree days) changes.

## Data collection methods and equipment
- Equipment:
  - Automated Weather Station (AWS) for meteorological data; multiple sensors (air temp, humidity, rainfall, solar radiation, PAR, net radiation, wind).
  - Micro-meteorological sensors in plots for soil temperature and soil moisture (5, 10, 20 cm depths; TDR sensors post-2008).
  - Ground-level rain gauges and Warren spring collectors for rainfall and chemistry.
  - Plot-level throughfall collectors; lysimeters and tensioned samplers for soil water chemistry.
  - CO2/CH4/N2O measurement systems (IRGA, CIRAS-2, LI-COR equipment) for soil respiration and trace gas fluxes.
  - Litter traps, pin-point vegetation surveys, canopy reflectance measurements (ground-based spectrometer), and phenology assessments.
  - Soil cores and collars for root biomass, microbial biomass via chloroform fumigation, mineralisation studies, SOM/SOC/bulk density.
- Data frequency and timeline:
  - AWS: minute- to hourly-averaged data; daily summaries (1999–present).
  - Micro-met: minute-based, later hourly/half-hour averages (1998–present).
  - Rainfall/throughfall: biweekly (site rainfall), plot-level throughfall biweekly; data gaps handled with exclusion or infill as needed.
  - Soil respiration, trace gases, NEE, photosynthesis, vegetation biomass, and other biogeochemical measures follow varying schedules (fortnightly, monthly, annual, or episodic over years).
- Data processing highlights:
  - Data are converted to flux units (e.g., mg CO2-C m-2 hr-1) with instrument-specific conversion factors (CIRAS-2, LICOR 8100, LI-8100A).
  - NEE and photosynthesis adjusted for biomass differences across chamber bases using above-ground biomass data.
  - Pin-point vegetation data converted to biomass using calibration factors; year-to-year quadrat surveys aligned with fixed base pegs.
  - Canopy reflectance values computed as NDVI (680 and 570 nm bands) and PRI indices.
  - Throughfall computations apply percent-difference methodology relative to site rainfall to derive plot-level rainfall; data gaps excluded or infilled with year-averaged reductions.
- Data quality control:
  - Visual QC via spreadsheets; manual checks noted due to historical data practices; older datasets may lack some documentation of processing steps.

## Data processing, quality control, and units
- Data processing notes:
  - Legacy data may not meet modern best-practice documentation standards.
  - Multiple sensors and instruments used over time require careful unit conversions and cross-calibration (e.g., CO2 flux conversions between g CO2 m-2 h-1, µmol m-2 s-1).
  - NEE and respiration data require biomass normalization to compare treatments.
- Common processing themes:
  - Consistent data aggregation (minute to hourly to daily).
  - Use of calibration equations and published coefficients for converting pin hits to biomass for vegetation components.
  - Explicit handling of missing or compromised data (e.g., exclusion of certain plots or data points when measurement integrity is uncertain).

## Data availability and contact
- Not all data are stored in the EIDC or centralized repository; contact details provided for data access and further information:
  - Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Timeframes and data scope vary by dataset; detailed institutional contact is advised for dataset-level access and provenance.

## Data quality challenges and caveats
- Patchy data across years and formats, with method changes over time (e.g., soil respiration instruments, micro-meteorological sensors).
- Throughfall data can be compromised by equipment loss or damage (funnel or bottle issues) requiring plot-level exclusion or infill with average reductions.
- Automated warming/drought curtains limited by wind, leading to occasional data gaps or partial treatment application.
- Some datasets (trace gases, NEE, etc.) have limited temporal coverage (episodic measurements in specific years).
- Documentation for some legacy data processing steps may be incomplete or not aligned with current best practices.

## Appendices and layout (data context)
- Appendix 1: Site layout and plot/quadrat arrangement; grid references and plot numbering.
- Appendix 2: Quadrat layout and measurement areas, with defined codes for vegetation components.
- Appendix 3: Plot layout with quadrats and measurement zones.

## Practical notes for data users
- Useful for validating ecosystem responses to drought and warming in upland moorland ecosystems.
- Enables cross-dataset analyses linking meteorology, hydrology, soil processes, and vegetation responses over long time scales.
- Requires careful attention to provenance, measurement methods, and cross-instrument calibration when integrating data across years.