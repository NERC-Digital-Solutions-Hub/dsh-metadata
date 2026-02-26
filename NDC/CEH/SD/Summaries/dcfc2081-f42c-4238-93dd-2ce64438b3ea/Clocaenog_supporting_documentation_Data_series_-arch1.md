# Climoor field site in Clocaenog forest Supporting documentation for data

- Climoor is a climate change manipulation experiment in Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years. The site, established in 1998, is an upland moorland dominated by Calluna vulgaris (heather) with a soil type described as humo-ferric podzol. The system is designed to run on solar and wind power.

- Treatments and layout
  - Two climate treatments: drought and warming, each replicated on three plots.
  - Three control plots mirror shading from the experimental structure.
  - Total plots (n=9) arranged in blocks.
  - Drought treatment operates to reduce rainfall during the growing season; timing has varied (May–Sept historically; since 2012, April–October). Typical annual rainfall reduction ~20%, with greater reductions during the growing season (~79% in peak years).
  - Warming treatment uses retractable aluminium curtains to reduce nighttime heat loss; rainfall can be partially excluded due to a rain-detection-triggered roof retraction, resulting in about ~14% annual rainfall reduction. Curtains are not operated in winds above 10 m s-1.

- Location and environment
  - Location: Clocaenog Forest, Wales (coordinates provided in site documentation).
  - Ecosystem: Wet upland heath with dominant evergreen heather; a mix of Vaccinium myrtillus, Empetrum nigrum, bryophytes, and other vegetation.
  - Soil: Humo-ferric podzol with variable horizons (E and Bh not always visible); parent material mainly Ordovician–Silurian shale/mudstone.

- Data types and data producers (summary of datasets)
  - Weather and microclimate
    - AWS meteorological data: daily measurements since 1999 (air temp, humidity, rainfall, solar radiation, net radiation, PAR, wind, pressure).
    - Micro-meteorological plot data: daily soil/air temperature and soil moisture (from 1998 onward; various sensor types over time).
  - Hydrology and rainfall
    - Site rainfall (storage rain gauge, biweekly) and rainfall chemistry (pH, nitrate, chloride, sulfate, DOC, ammonium).
    - Throughfall data (plot-level rainfall, biweekly) used to compute treatment-specific rainfall changes.
    - Water table depth via permeable tubes (installed 2009; biweekly measurements).
  - Soil and root processes
    - Soil respiration (fortnightly and high-resolution; soil collars; various instrumentation across years).
    - Trace gases (CH4 and N2O) measured with static chambers (in the same collars as soil respiration).
    - Net ecosystem CO2 exchange (NEE) measured in select years (2002–2004, 2011) with chamber systems and CO2 analyzers; adjustments for biomass differences.
    - Photosynthesis (ambient and response curves) for major shrub/instrumental measurements (2001–2007; 2002–2003 light and CO2 response curves for Calluna and Vaccinium).
  - Vegetation and plant–soil interactions
    - Vegetation survey data (Pin-point biomass estimates) across multiple years (1998–2012, with earlier and later measurements); biomass conversion factors provided.
    - Canopy reflectance (NDVI and PRI) from 2001–2004.
    - Phenology, annual growth, and pathogen assessments for key species (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum) across several years.
    - Vegetation chemistry (green and litter material) for C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates.
    - Litterfall measurements (1999–2002; annual means reported with unit conversions).
  - Soil biochemistry and biology
    - Root biomass (various years; multiple core methods) and soil microbial biomass (chloroform fumigation with DOC analysis).
    - Nitrogen mineralisation experiments (1998–2004) with ammonium/nitrate in KCl extracts.
    - SOM, SOC and bulk density derived from paired cores; depth and horizon details captured.
    - Soil solution and leachate chemistry (pH, NO3, Cl, SO4, DOC, NH4) from lysimeters and tensioned samplers (1998–2008).
  - Appendices
    - Site layout and quadrat/plot configurations for replicability and spatial reference.

- Data processing, quality, and notes
  - Data come from multiple instruments and methods; harmonization requires careful unit conversions and cross-method calibrations (e.g., soil respiration units, NEE conversions, etc.).
  - Historical data include legacy processing steps; some datasets may not reflect current best practices for data documentation.
  - Quality control includes basic visual checks and field notes; some gaps exist due to equipment failures, calibration gaps, or data loss.
  - Throughfall and rainfall data require adjustments to estimate plot-level rainfall changes from site-level measurements; data gaps result in plot exclusion or infill with year-average reductions where needed.
  - Datasets are hosted in on-site portals (e.g., EDIC/EIDC) with metadata; some data after June 2015 may not be stored in the same repository. Contact CEH Bangor for access and details.

- Accessibility and contact points
  - The documentation notes that not all data are stored in a single repository; contact Sabine Reinsch and Bridget Emmett at CEH Bangor for data details and access.
  - Summary tables and supporting documentation accompany datasets to assist understanding of methods, units, and calibration factors.

- Practical implications for analysis
  - The dataset enables analysis of the effects of drought and warming on carbon and nitrogen cycling, soil respiration, trace gas fluxes, plant biomass and phenology, litter inputs, and soil chemistry.
  - Rich time series (1998–2015) across abiotic and biotic responses allow correlations and predictive modeling of ecosystem responses to climate manipulation.
  - Researchers should account for missing data, older measurement practices, and dataset-specific unit conversions when performing cross-dataset analyses.

- Appendix highlights
  - Appendix 1: Site and plot layout, including grid references and block structure.
  - Appendix 2: Quadrat layout and measurement areas across plots.