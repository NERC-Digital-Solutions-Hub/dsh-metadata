# Climoor field site in Clocaenog forest Supporting documentation for data

- An automated climate-manipulation experiment at Clocaenog Forest, North East Wales, established in 1998 to simulate drought and warming treatments affecting upland moorland vegetation.
- Treatments involve drought and warming in replicated plots with a control, using roof-based and curtain-based technologies operated to reflect climate-change predictions for the next 20–30 years.
- Rich, multi-parameter data collection across abiotic and biotic variables over multiple years, with detailed methodologies and site layout.

## Location, site characteristics and ecosystem

- Location: Clocaenog Forest, North East Wales (grid reference SJ019519; 53°03'19"N, -03°27'55"W; approx. 53.055°N, 3.465°W).
- Ecosystem: upland west-atlantic moorland dominated by Calluna vulgaris (heather); accompanying species include Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, and various bryophytes.
- Soil: humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons (E typically 6–17 cm depth where present).
- Plot scale: 4 m x 5 m plots arranged in blocks; 3 replicates per climate treatment (warming W, drought D) and 3 control plots (C) across 3 blocks.

## Climate change treatments and experimental design

- Treatments and replication:
  - Warming (W): 3 plots
  - Drought (D): 3 plots
  - Control (C): 3 plots
  - Total: 9 plots with block structure (Block 1–3; varied assignment of treatments across blocks).
- Drought treatment:
  - Implemented with retractable polyethylene roof to exclude rainfall; originally May–Sept (1999–2011) to mimic UK droughts; from 2012, April–October.
  - Rainfall reduction: approximately 20% annually; up to ~80% of rainfall excluded during the growing season; some small events may still be detected depending on sensor limits.
  - Wind control: curtains do not operate in winds >10 m/s.
- Warming treatment:
  - Retractable aluminium mesh curtains; reflect 96–97% of infrared radiation; reduces night heat loss; roof operation linked to light/dark cycles; rain sensors trigger retraction to protect warming when rain occurs; rainfall reduction about 14% annually.
  - Wind limitations similar to drought treatment.
- Spatial layout and references:
  - Appendix 1–3 provide site layout, quadrat layout, and plot references.
  - Data tables include site coordinates and a detailed mapping of treatment assignments by block.

## Equipment, data protocols and data processing

- On-site data collection framework:
  - AWS met data: automated weather station with a suite of meteorological sensors; data logged daily and archived (1999–present; year-by-year variations exist).
  - Micro-meteorological plot data: soil temperature (5, 10, 20 cm) and soil moisture (TDR, 2008 onward; earlier methods noted); daily sampling with hourly averages.
  - Abiotic and biotic data streams include rainfall (site-level storage gauge and rainfall chemistry), throughfall (plot-level rainfall), water table depth, soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation biomass, canopy reflectance, phenology, vegetation chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC and bulk density, and soil solution/leachate chemistry.
- Data structure and quality:
  - Many datasets span 1998–present with varying sampling frequencies (daily, weekly, biweekly, monthly, yearly).
  - Earlier years use older equipment; later years show transitions to newer instruments (e.g., CIRAS-2 to LI-COR systems for respiration; automated soil respiration campaigns in 2013–2014).
  - Data quality control generally relies on visual checks (Excel-based) and cross-method conversions; some legacy data processing steps are not fully documented according to current best practices.
- Data conversions and units:
  - Standardized outputs described for converting instrument-specific units to mg CO2-C m-2 h-1 or related flux metrics.
  - Calibration details and methodological notes provided for each data stream (e.g., soil respiration conversion factors, NEE adjustments for biomass, etc.).

## Datasets and methodological highlights (selected)

- AWS meteorological data: minute-level sensors (temperature, humidity, rainfall, solar and PAR, wind, pressure); hourly averages; long-term site data.
- Micro-meteorological data: plot-level soil temperature and moisture; high-frequency measurements with modern sensors introduced mid-era.
- Rainfall and rainfall chemistry: site-level storage gauge with biweekly rain samples; pH, nitrate, chloride, sulfate, DOC, ammonium analyses to CEH lab standards.
- Throughfall data: plot-level rainfall captured biweekly; adjustments applied to estimate plot rainfall relative to site rainfall; data quality flagging for missing/compromised measurements.
- Water table depth: permeable tubes; biweekly readings; maximum detectable depths per plot specified.
- Soil respiration and trace gases: multi-era measurement approaches (CIRAS-2, LICOR 8100, automated LI-COR systems); flux calculations via linear regression of CO2 concentrations over time; CH4 and N2O measured via static chambers and GC analysis with calibration protocols.
- Net ecosystem CO2 exchange (NEE): measurements in 2002–2004 and 2011 with different chamber systems; respiration fluxes separated by light/dark incubation in later years; biomass-adjusted fluxes using pin-point-derived above-ground biomass.
- Photosynthesis: ambient measurements and response curves (PAR and Ci) for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum; leaf-area considerations via leaf mass for standardization.
- Vegetation surveys (pin-point biomass): annual assessments (1998–2012) using 300-pin grids across three quadrats per plot; conversion of pin hits to biomass using species-specific calibration factors; adjustments for missing pins.
- Canopy reflectance: NDVI and PRI indices from ground-based spectrometry (2001–2004); 1637 spectral bands from 400–950 nm; background and species-specific reflectance captured.
- Vegetation phenology and growth: shoot elongation, budburst, leaf counts, and pathogen indicators across species; sampling windows April–September; multi-year growth measurements.
- Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates; green and senesced material analyses.
- Litterfall: monthly collection (1999–2002) with later reduced frequency; conversion to g m-2 and pooled-year analyses; CEH labs for carbon/nitrogen content.
- Root biomass and soil biota: core-based root extraction and imaging (WinRHIZO) across several years; microbial biomass via chloroform fumigation; mineralisation and SOM/SOC/bulk density assessments.
- Soil solution and leachate chemistry: lysimeters and tension samplers; pH, NO3, Cl, SO4, DOC, ammonium analyses; samples processed within standard lab timelines.

## GIS-ready, spatial and data-structure implications

- Plot and quadrat layouts: Appendix 1–3 provide explicit plot and quadrat configurations, enabling mapping of measurement points, plot boundaries, and sampling frames.
- Spatial references and scale:
  - Plots are fixed at 4 m x 5 m with defined block structure; site coordinates enable GIS integration and spatial analyses of treatment effects.
  - Throughfall, rainfall partitioning, soil moisture, and vegetation metrics are associated with plot-level locations for spatial aggregation or time-series GIS visualizations.
- Data availability and access notes:
  - Not all data are stored in a single centralized system (EIDC); some datasets post-2015 may reside outside standard repositories.
  - For further detail or access, contact Sabine Reinsch and Bridget Emmett at CEH Bangor.

## Usage considerations for GIS specialists

- Data harmonization: multiple datasets span different years and instruments; careful alignment of time scales, units, and plot identifiers is required for map-based analyses and temporal visualizations.
- Data gaps and quality: legacy data documentation varies; some processing steps are not fully documented; anticipate gaps or infill in older datasets when building GIS products.
- Potential map layers:
  - Plot-level climate treatment fields (W/D/C) by year; block layout visualization.
  - Time-series layers for abiotic (soil moisture, rainfall, temperature) and biotic (biomass, phenology, leaf chemistry) variables by plot.
  - Canopy reflectance indices over plots linked to species composition and biomass data.
  - LIDAR or high-resolution canopy structure could be integrated with pin-point biomass and litterfall data for multi-layered vegetation maps.

## Contact and further information

- Data inquiries and data processing details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.