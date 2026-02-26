# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment in Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
- Site characteristics: upland moorland with Calluna vulgaris-dominated vegetation; humo-ferric podzol soil; established 1998; powered by solar/wind.
- Study design includes drought and warming treatments with replicates and controls, alongside a detailed suite of abiotic and biotic data streams for long-term ecological analysis.

## Data inventory and scope
- Data streams collected (years span 1997–2015 and beyond as indicated): 
  - AWS meteorological data (daily; air temp, RH, rainfall, pressure, net radiation, solar radiation, PAR, wind)
  - Micro-meteorological plot data (soil/air temperature, soil moisture)
  - Rainfall data (storage rain gauge; biweekly collection) and rainfall chemistry
  - Throughfall data (plot-level rainfall; biweekly)
  - Water table depth (biweekly)
  - Soil respiration (fortnightly and automated campaigns)
  - Trace gases (CH4, N2O) measurement
  - Net ecosystem CO2 exchange (NEE)
  - Photosynthesis data
  - Vegetation survey data (plant biomass; Pin-point method)
  - Canopy reflectance (NDVI and PRI indices)
  - Vegetation phenology, annual growth, and pathogen assessment
  - Vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates)
  - Litterfall (monthly/annual; 1999–2002; later less frequent)
  - Root biomass (multiple methods across years)
  - Soil microbial biomass (chloroform fumigation method)
  - Nitrogen mineralisation (extractable ammonium/nitrate)
  - SOM, SOC and bulk density
  - Soil solution and leachate chemistry (lysimeters and tensioned samplers)
- Data management note: not all data are stored in the EIDC; some smaller or post-2015 datasets may be stored separately.  
- Data documentation and metadata: each dataset has an associated supporting documentation file (RTF) and a dataset name (CSV) for discovery and reuse.

## Data collection protocols and processing
- Climate change treatments:
  - Drought: retractable polyethylene roof reducing rainfall by ~20% on average during May–Sept (and since 2012 Apr–Oct). Roofs do not operate in high wind (>10 m/s). Data indicate annual and growing-season rainfall reductions (vary by year; site occasionally misses small rain events).
  - Warming: retractable aluminum curtains reflect infrared radiation, with nightly operation guided by light sensors; rainfall reduction (~14% on average) occurs due to rain retraction logic; winds can limit operation.
  - Experimental design: 9 plots total (3 warming, 3 drought, 3 controls) arranged in blocks; shading from treatments mirrored in controls.
- Equipment and data collection:
  - AWS met data: high-frequency (minute-level; hourly averages) meteorological measurements; site-mounted 4 m mast after 2007 due to theft risk.
  - Micro-meteorological plot data: daily measurements of soil and air temperature, soil moisture (TDR and earlier methods).
  - Rainfall and rainfall chemistry: biweekly sampling; sample processing includes pH, NO3, Cl, SO4, DOC, ammonium analyses using standard lab methods.
  - Throughfall: plot-level rainfall captured; data used to compute treatment percent changes applied to site-level rainfall to derive plot-level rainfall, with exclusions for data loss.
  - Water table depth: measured biweekly from bedrock downward via permeable tubes (max detectable depths per plot listed).
  - Soil respiration and trace gases: multiple measurement methods over time (CIRAS-2, LICOR 8100, automated LI-COR systems; soil collars installed; automated campaigns in 2013–2014).
  - NEE and photosynthesis: measured with chambers and IRGA systems; adjustments for biomass due to variable plot vegetation.
  - Vegetation and canopy: Pin-point biomass calibration; canopy reflectance (NDVI and PRI); phenology and growth measurements; litterfall; root biomass (multiple core methods); soil microbial biomass; nitrogen mineralisation; SOM/SOC/bulk density; soil solution chemistry.
- Data processing notes:
  - Legacy data include varied instrumentation and documentation quality; conversions between measurement units documented (e.g., between g CO2 m-2 h-1, µmol m-2 s-1, and mg C m-2 h-1).
  - Pin-point vegetation biomass uses species-specific calibration factors; 1998–2012 time series with occasional gaps filled using year-specific conversion factors.
  - Throughfall data are validated by cross-checking with site-level rainfall data; some treatment means may exclude plots if data are compromised.
  - Data quality control primarily through manual visual checks; no uniform automated QC thresholds across all datasets due to historical practices.

## Metadata, provenance, and documentation
- Dataset naming conventions and supporting documentation provided for each data stream.
- Versioning: document indicates version 2 (dated 21/07/2015); some datasets note legacy processing practices.
- Documentation access: contact points for data details and clarifications (Sabine Reinsch and Bridget Emmett) with CEH Bangor email addresses.
- Appendix materials include site and plot layouts (Appendix 1: site details; Appendix 2: quadrat layout; Appendix 3: plot layout; LYS, PQ, SS markers).

## Data access, storage, and governance
- Storage and access:
  - AWS and many core datasets are stored in central repositories; some smaller or post-June 2015 datasets may be stored outside the EIDC.
  - Throughfall, rainfall chemistry, and other long-running measurements have explicit collection and processing protocols; data may be subject to gap-filling or exclusion rules when data quality is compromised.
- Governance considerations for Data Stewards:
  - Ensure complete metadata for all datasets, especially legacy data streams with inconsistent documentation.
  - Maintain clear version history and update paths as data streams evolve (instrument changes, processing methods, calibration factors).
  - Document data processing steps, including unit conversions and biomass adjustment factors, to enable reproducibility.
  - Capture data provenance, treatment assignments, and plot-level relationships to ensure correct interpretation of comparative analyses (treatment vs. control).
  - Establish and communicate data availability constraints (e.g., non-EIDC storage, legacy data gaps, post-2015 data handling) and contact points for data access.
  - Monitor and manage data quality issues arising from treatment implementation (e.g., data loss during high rainfall events, weather-driven operational limits).

## Particular challenges and considerations
- Incomplete or evolving understanding of user needs across long-term datasets.
- Timely acquisition of data from multiple instruments and teams; integration across diverse systems and formats.
- Ensuring metadata completeness for legacy data with heterogeneous documentation.
- Handling large, multi-year datasets with changing measurement methods and equipment.
- Data gaps due to instrument downtime, rainfall-related data losses, or treatment operation limits during high winds.

## Contacts and coordination
- Primary contacts for data access and clarification: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Additional site and layout details referenced in appendices.

## Appendix overview
- Appendix 1: Site layout and grid references.
- Appendix 2: Quadrat layout and quadrat identification (PQ, LYS, SS markers).
- Appendix 3: Plot layout with measurement areas indicated.