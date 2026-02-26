# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview

- Purpose: CINAg project to meet China and UK needs for optimizing farm practices and soil management to improve nitrogen use and reduce Nr losses, mitigating environmental impacts.
- Objectives:
  - Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil health metrics to guide farm practices.
  - Test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers via CAU/CAAS programs.
- Structure: Four work packages
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Data assets and data types

- Experimental data
  - Inorganic fertiliser grass trials (2016) across four UK platforms; digestate trials (2017) on winter wheat; additional grassland trials (2017–2018)
  - UK-wide soil and biomass sampling (2018)
  - Measurements: yields (dry matter, quality metrics), N content and N offtake, NUEc and NUEg calculations
- Greenhouse gases
  - Ammonia (NH3) volatilisation and nitrous oxide (N2O) fluxes; measurement methods include wind tunnels and static chambers; area-wide cumulative flux calculations
- Soil chemical and physical metrics
  - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N
  - Carbon and nitrogen pools: DOC, TDN, DON, MBC, MBN
  - Physical/chemical properties: pH, EC, soil texture, SOM, cations (Na, K, Ca, Mg), total C and N, total P, POXC, Olsen-P, extractable P forms
  - DNA and microbial genes: DNA extractions; qPCR targets (nifH, amoA, nirK, nirS, nosZ, ureC); OTUs and diversity indices
- Microbial ecology
  - Amplicon sequencing data (16S rRNA; ITS), diversity indices (Shannon, richness)
- Plant and biomass metrics
  - Above-ground biomass, grain and straw yields; quality metrics (CP, ME, NDF, ADF, D value, TGW)
- Meteorological and soil process data
  - Rainfall, air/soil temperatures, WFPS, soil moisture; wind data; infiltration rates; water release curves
- Data provenance and structure
  - Multi-site, multi-year design (NW, HA, HF, EB platforms; 2016–2018 UK-wide sampling)
  - Appendices and tables detailing site specifics, fertiliser regimes, harvest dates, sampling schedules

## Locations, platforms, and sampling scope

- Four UK farm platforms (2016–2017)
  - North Wyke (NW) – Devon
  - Harpenden (HA) – Herefordshire
  - Henfaes Farm (HF) – North Wales
  - Easter Bush (EB) – Scotland
  - Treatments include inorganic fertilisers and digestate; plots configured for emissions measurements and biomass sampling
- Nine UK-wide sites (2018)
  - Land uses across sites include pristine, grazing, arable, pasture, grass margins, and arable rotations
  - Sites span Scotland, Wales, and England with multiple land-use contexts per site
- Meteorology and site data
  - Site-specific weather stations and soil moisture sensors; long-term data at Easter Bush measurement station

## Data schemas, metadata, and documentation

- Experimental design and protocols
  - 2016 inorganic fertiliser grass trials: randomized blocks; treatments include Urea (U), Urea with inhibitor (IU), Ammonium-nitrate (AN), and Controls; full P/K/S fertilisation per Defra guidelines
  - 2017 digestate trials: randomized blocks; digestate treatments with/without acidification and nitrification inhibitor (DMPP); control plots
  - 2018 UK-wide sampling: diverse land uses with repeated measurements
  - Sub-plot and harvest layouts vary by site and year; detailed in appendices
- Sampling schedules
  - WP1: soil sampling at defined intervals (before treatments, after harvests, etc.)
  - WP2: intensified soil sampling following fertiliser applications; frequent sampling early on, tapering over time
- Data processing and analytics
  - Yields and biomass: standardized on dry matter basis; quality metrics derived from NIR analyses
  - NUE calculations: NUEc and NUEg using crop N offtake and applied N
  - Emissions: NH3 flux quantified from wind tunnels and dispersion models; N2O flux via manual and automatic chambers
  - Soil nutrients: NH4+, NO3-, amino acids, minerals; DOC/TDN; mineralisable N
  - Soil properties: POXC, extractable P forms, Olsen-P, soil C and N, pH, EC, cations
  - DNA/microbial data: qPCR results; amplicon sequencing pipelines; rarefaction and diversity metrics
  - Hydrology and physics: infiltration and water release curves; HYPRO/Durner-based modelling for soil moisture relations
- QA/QC practices
  - Laboratory standards (BS1/BS3), random replicates, instrument calibration, and cross-lab QA checks
  - Consistent data curation in spreadsheets and LIMS; manual and automated checks prior to release
- Data processing tools
  - R (various versions), packages such as pracma; Bayesian analysis with JAGS (MCMC); area-under-curve calculations; custom scripts for NH3/N2O flux modelling

## Access, sharing, and governance

- Project portal and publications
  - Public project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Related publications (2018) documenting dataset-derived insights
- Data stewardship
  - Contributors from multiple institutions (CEH, Rothamsted, Bangor, etc.); clear protocols and standardized methods to enable data reuse
  - Datasets designed to support open-access reporting and further research within the CINAg program and beyond

## Implications for Data Leaders

- Data strategy goals illustrated
  - Build a cohesive, multi-site data platform that tracks experimental design, site metadata, and longitudinal measurements
  - Develop holistic NUE and soil-health metrics enabling cross-site comparability and actionable farm guidance
- Best practices to adopt
  - Standardized metadata schemas and harmonized naming conventions across sites and years
  - Comprehensive data provenance: document methods, instruments, calibrations, and QA/QC steps
  - Centralized data catalog with clear data licenses, access controls, and versioning
  - Reproducible analytics: share code (R, JAGS) and processing pipelines; maintain documentation for reproducibility
  - Integrated data governance: manage data quality, lineage, and updates; coordinate across collaborating institutions
- Challenges to address
  - Handling heterogeneous data collection across diverse sites and laboratories
  - Ensuring consistent temporal and spatial resolution for cross-site comparisons
  - Balancing comprehensive measurement with practical field constraints and data volume
- Value for strategic decision-making
  - Rich, multi-modal datasets enable robust NUE indicators and soil-health metrics
  - Framework supports translating scientific insights to farming practices and knowledge exchange with stakeholders (including international partners)