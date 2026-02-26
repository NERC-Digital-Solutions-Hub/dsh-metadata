Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Automated climate change manipulation experiment in upland moorland (Clocaenog Forest, North East Wales) using drought and warming treatments.
- Treatments implemented on replicated plots with on-site solar and wind power; designed to reflect 20–30 year climate predictions.
- Site established in 1998 with 9 plots (3 warming, 3 drought, 3 controls) arranged in 3 blocks; scaffolding mirrors shading on treatment plots.

## Spatial and Temporal Scope
- Location and grid: Clocaenog, Wales; grid reference SJ019519; coordinates 53.055°N, -3.465°W.
- Habitat: Wet upland heath dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum; detailed plant list provided.
- Plot layout: 4 m x 5 m plots; 3 treatments (warming, drought) plus 3 controls per block; 9 plots total.
- Appendix references: Appendix 1 (site layout) and Appendix 2 (quadrats); 2012 plot layout details.
- Data timeframes: 
  - Drought treatment active intermittently from 1997–2014 (expanded season over time); 1999–2011 most years.
  - Warming data recorded from 1997 onward with varying reporting through 2014.
  - Data types span 1998–present for many datasets; some series are earlier or limited.

## Data Types and Datasets (GIS-relevant variables)
- AWS meteorological data: daily meteorological measurements (air temp, humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind) from an on-site AWS; daily, 1999–present.
- Micro-meteorological plot data: daily plot-level soil and air temperature, soil moisture; 1998–present.
- Rainfall and rainfall chemistry (site-level): biweekly rainfall totals and chemistry (pH, NO3, Cl, SO4, DOC, ammonium); 1998–present.
- Throughfall data (plot-level rainfall): biweekly; used to compute percent change relative to site rainfall; data quality checks and occasional infill.
- Water table depth: biweekly measurements from 2009–present via permeable tubes to bedrock.
- Soil respiration: fortnightly measurements (manual and automated) with multiple chamber systems; 1999–present, across plots; includes CO2 flux conversions.
- Trace gases (CH4 and N2O): measurements using soil collars and static chambers; sampling at 0.25, 15, and 30 minutes; analyzed by GC; 1999–2000, 2007–2009.
- Net ecosystem CO2 exchange (NEE): selective years (2002–2004, 2009–2011) with different instrumentation; flux conversions and biomass-adjusted analyses.
- Photosynthesis: infrequent measurements (2001–2003) using IRGA and leaf cuvettes; standardized light conditions.
- Vegetation survey data (pin-point biomass): annual biomass estimates (1998–2012) via pin-point method across three quadrats per plot; includes biomass calibration and conversion factors.
- Canopy reflectance: ground-based spectral measurements (NDVI and PRI indices) for select years (2000–2004); spectral bands 400–950 nm; nadir measurements.
- Vegetation phenology, annual growth and pathogens: annual shoot elongation and phenophase observations for C. vulgaris, V. myrtillus, E. nigrum; 1998–current; includes budburst, leaf counts, and pathogen signs.
- Vegetation chemistry: elemental composition (C, N, P, K, Ca, Mg), lignin, tannin, alpha-cellulose, carbohydrates; samples from green and litter; annual analyses.
- Litterfall: monthly (1999–2002) and periodic thereafter; pooled quadrat samples converted to g m^-2; carbon and nitrogen analyses.
- Root biomass: multiple methods across 2003–2013 (soil cores, washing, WinRHIZO analysis for some years).
- Soil microbial biomass: chloroform fumigation–extraction (2000, 2001, 2012).
- Nitrogen mineralisation: core-based incubations (1998–2004) with nitrate and ammonium analyses.
- SOM, SOC and bulk density: soil core analyses (1999–2004, 2013) with density and carbon calculations.
- Soil solution and leachate chemistry: lysimeters and tensioned samplers (biweekly sampling 1998–2008); analyses for pH, NO3, Cl, SO4, DOC, NH4.

## Data Collection, Processing and Units
- Equipment and data collection:
  - AWS sensors mounted on a 4 m mast after 2007 thefts; minute-level measurements aggregated to hourly.
  - Micro-mete plot sensors measure soil temperature and moisture; daily/hourly scales.
  - Rainfall and throughfall collectors (gauge-based and plot-level bottles).
  - Soil respiration and trace gas measurements using closed systems with chamber-based methods; multiple instrument configurations over time.
  - Canopy reflectance via ground-based spectrometer; NDVI and PRI calculations.
- Data processing notes:
  - Legacy data exist; some datasets lack complete documentation of processing steps.
  - Unit conversions for flux data (e.g., g CO2 m^-2 h^-1 and μmol m^-2 s^-1) to mg C m^-2 h^-1 described for NEE and respiration.
  - Pin-point biomass conversion factors established from destructive calibration in 2000; careful QA of pin data and pin counts.
  - Throughfall data require adjustment to align with site rainfall for seasonal/annual estimates; plots may be excluded if data are compromised.
  - Biomass and chemistry data typically converted to per m^2 bases using standard soil/biomass conversion factors.

## Data Quality, Provenance and Access
- Quality control:
  - Daily and hourly data quality checks described for AWS and micro-meteorological data; visual QC in Excel noted as primary method.
  - Some data were stored outside the main data hub (EIDC); not all infrequent or post-2015 data are guaranteed to be stored in the EIDC.
  - Throughfall and rainfall data include methods for handling data gaps and infill with year-average reductions when necessary.
- Provenance and contacts:
  - Primary contact points: Sabine Reinsch and Bridget Emmett (CEH Bangor); for data details and access.
  - Data processing notes indicate multiple instrument changes and methodological shifts over time; some documentation reflects legacy practices.

## Spatial Details and GIS Considerations
- Plot/experimental layout:
  - 9 plots in total (3 warming, 3 drought, 3 controls) arranged in blocks; Appendix 2 provides quadrat layout; Appendix 1 shows site layout.
  - 4 m x 5 m plot footprint; treatment structures and shading reflectance captured in site design.
- Site characteristics:
  - Soils: humo-ferric podzol with variable eluvial and illuvial horizons (E and Bh horizons).
  - Vegetation and biomass data tied to specific taxa (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, etc.).
- GIS integration:
  - Data can be joined to plot IDs and blocks for spatial analyses of treatment effects.
  - Can support map-based visualization of treatments, biomass distributions, soil properties, and flux datasets.
  - Spatial references and plots enable creation of choropleth maps of treatment effects over time and across years.

## Practical Considerations for GIS Specialists
- Data availability and resolution:
  - Many time-series datasets exist at plot or site level; some high-resolution spatial data are limited to plot-level measurements.
  - Data gaps and historical changes in instrumentation should be accounted for in analyses and visualizations.
- Standardization and harmonization:
  - Align units across datasets (e.g., CO2 flux units, soil moisture, nutrient concentrations) for cross-dataset analyses.
  - When combining datasets (e.g., NEE with biomass), apply biomass-adjusted corrections as documented.
- Suggested GIS workflows:
  - Build a plot-level spatial layer with attributes: treatment (W/D/C), block, plot area, coordinates, and time-series keys.
  - Link time-series datasets via plot IDs and date fields to create interactive maps or dashboards showing treatment effects over time.
  - Compute derived metrics (e.g., percent rainfall reduction, NDVI indices, flux conversions) for mapping or temporal trend visualization.
- Reference and reproducibility:
  - Maintain metadata about data provenance, sensor changes, and processing steps to ensure reproducibility.
  - Use the Appendix layout (site and quadrat maps) to validate spatial relationships and ensure accurate georeferencing.

## Access and Contact
- Data and supporting materials are maintained by CEH Bangor (Alwyn Sowerby; edited by Sabine Reinsch; contact through Sabine Reinsch and Bridget Emmett).
- Some datasets are not fully centralized in the EIDC; for clarification or data requests, contact CEH Bangor representatives listed in the dataset documentation.