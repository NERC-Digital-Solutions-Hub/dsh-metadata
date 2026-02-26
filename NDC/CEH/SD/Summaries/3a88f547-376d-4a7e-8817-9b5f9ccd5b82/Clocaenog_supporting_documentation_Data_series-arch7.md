# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Documentation of a climate-change manipulation experiment (Climoor) using automated roof technology to create drought and warming treatments reflecting 20–30 year climate predictions.
- Focus on data generation, measurement methods, and datasets across abiotic and biotic variables.
- Data intended for GIS-friendly visualization and analysis, with emphasis on spatial layout (plots, quadrats) and temporal measurements.

## Location and Site Context
- Location: Clocaenog Forest, North East Wales, UK (53°03'19''N, 03°27'55''W).
- Ecosystem: upland west-atlantic moorland; dominant vegetation includes Calluna vulgaris (heather) >60% of biomass; other species present listed.
- Soil: humo-ferric podzol with variable horizons (E and Bh) and depth ranges described; site characteristics summarized in Table 1.
- Establishment: site established in 1998; designed for solar/wind power support and remote operation.

## Climate Change Treatments
- Treatments and replication:
  - Drought: 3 replicate plots
  - Warming: 3 replicate plots
  - Controls: 3 plots with scaffolding to mirror shading effects
  - Plot size: 4 m x 5 m
  - Total plots: 9
- Treatment details:
  - Drought: retractable polyethylene roof reducing rainfall by ~20% (net reduction variable by year; some small events missed). Operated May–Sept 1999–2011; since 2012, April–October.
  - Warming: retractable aluminum mesh curtains reducing infrared loss; roof retracted during rain to maintain rainfall; average annual rainfall reduction ~14%.
  - Wind constraints: curtains do not operate in winds >10 m/s to prevent damage.
- Timing and year-to-year variation provided (Tables 2a, 2b summaries).

## Experimental Layout and Spatial Context
- Plot configuration: 9 plots arranged in blocks; each plot 4 m x 5 m; block and treatment allocation varies by year.
- Appendix 1: Site layout; Appendix 2: Quadrat layouts; Appendix 3: Plot layout with quadrats and measurement areas.
- Grid references and coordinates:
  - Grid Reference: SJ019519
  - Latitude/Longitude: 53.055 N, -3.465 W
- Vegetation and canopy context captured through point quadrats and biomass/phenology assessments (see below).

## Equipment, Protocols and Data Processing Framework
- On-site data infrastructure:
  - Automated Weather Station (AWS) for meteorological data (daily to current-day).
  - Micro-meteorological sensors in plots for plots-level measurements (daily).
  - Rainfall collection and chemistry sampling; throughfall measurements; lysimeters for soil solutions.
  - Periodic soil, vegetation, litter, and microbial sampling.
- Data processing approach:
  - Multiple data streams converted to common flux units (e.g., mg CO2-C m-2 h-1 for respiration/NEE).
  - Data quality controlled via basic visual QC (Excel) rather than automated strict limits (noted as a legacy data caveat).
  - Some datasets stored in the Environmental Information Data Centre (EIDC); not all datasets are stored there post-2015.
  - Data accessibility contacts provided for further details.

## Data Types and Datasets (Summary)
- AWS meteorological data (daily; minute-logged sensors; temperature, humidity, rainfall, radiation, wind, etc.).
- Micro-meteorological plot data (daily; soil and air temperature, soil moisture; depth up to 20 cm/10 cm).
- Rainfall data:
  - Storage rain gauge (site-level rainfall; biweekly collection).
  - Rainfall chemistry from Warren spring collectors (pH, NO3, Cl, SO4, DOC, ammonium).
- Throughfall data (plot-level rainfall; biweekly; used to derive plot-specific rainfall changes).
- Water table depth data (biweekly; permeable tubes from 2009 onward; maximum detectable depths per plot).
- Soil respiration data (fortnightly; collar-based chamber methods; multiple instrument eras; standardized to mg CO2-C m-2 h-1).
- Trace gases (CH4 and N2O) data (static chamber method; sampling at 0.25, 15, 30 minutes; GC analysis).
- Net Ecosystem CO2 Exchange (NEE) data (2002–2004, 2009–2011; chamber-based; flux units converted to mg CO2-C m-2 h-1; biomass-adjusted).
- Photosynthesis data (ambient and response curves; two datasets: ambient measurements and response curves; leaf-area considerations via mass measurements).
- Vegetation survey data (Pin-Point biomass; 1998–2012; 3 quadrats per plot; 100 pins per quadrat; conversion to biomass via calibration).
- Canopy reflectance (NDVI and PRI indices; 2000–2004; ground-based spectrometry).
- Vegetation phenology, annual growth and pathogen assessment (shoot elongation, budburst, growth metrics; 1998–present in varying cadence).
- Vegetation chemistry (green and senesced material; carbon, nitrogen, phosphorus, potassium, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates).
- Litterfall (monthly 1999–2002; yearly thereafter; weight and carbon/nitrogen analysis).
- Root biomass (multiple years; severed cores; varied methods across years).
- Soil microbial biomass (chloroform fumigation method; 2000, 2001, 2012).
- Nitrogen mineralisation (1998–2004; paired cores; nitrate and ammonium analyses).
- SOM, SOC and bulk density (derived from mineralisation cores; standard soil physics methods).
- Soil solution and leachate chemistry (lysimeters and tensioned samplers; biweekly to monthly sampling; pH, nitrate, chloride, sulfate, DOC, ammonium).

## Data Details and Measurement Methods (Representative Notes)
- Sensors and methods span a wide temporal range and multiple instrument families; conversions between raw units and mg CO2-C m-2 h-1 are documented for respiration and NEE datasets.
- Data lineage notes:
  - Legacy data with some undocumented processing steps.
  - Throughfall and plot-level datasets include handling for data loss and occasional infilling.
- Data quality and accessibility:
  - Primary data sources and contact points for detailed data inquiries: Sabine Reinsch and Bridget Emmett (CEH Bangor).
  - Data may be partially stored in EIDC; post-2015 data may reside outside EIDC.

## Accessibility, Documentation, and Notes
- Primary contact for data details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk).
- Data are described as not uniformly stored in EIDC; some datasets require direct inquiry.
- The document includes detailed tables, grid references, and conversion notes to support GIS-based interpretation and integration with other spatial datasets.

## Appendices and Figure/Layout References
- Appendix 1: Site layout overview.
- Appendix 2: Quadrat layout with measurement areas and quadrat codes.
- Appendix 3: Plot layout with quadrats and measurement areas; includes example subplot markers and plot identifiers.
- The layout documents lysimeters (LYS), pin quadrats (PQ), soil suction samplers (SS), and overall plot geometry for GIS alignment.