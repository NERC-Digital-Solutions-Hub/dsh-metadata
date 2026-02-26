# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- The CINAg project aims to optimise farm practices and soil management to use nitrogen sources more effectively and reduce environmental losses, with knowledge transfer between the UK and China.
- Objectives and structure:
  - Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil-health metrics.
  - Test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers via the Science and Technology Backyard programme.
  - Work Packages (WP): 
    - WP1: Improved understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange

- Project footprint and platforms:
  - Four UK farm platforms (2016–2017):
    - North Wyke (NW) — Devon
    - Harpenden (HA) — Herefordshire
    - Henfaes Farm (HF) — North Wales
    - Easter Bush (EB) — Edinburgh
  - 2018 cross-UK soil sampling at nine sites across Scotland, Wales, and England with diverse land uses.
  - Spatial data include coordinates, soil types, textures, mean annual temperature (MAT), and mean annual rainfall (MAP).

- Experimental design and timelines:
  - 2016: Inorganic fertiliser experiments on grassland at NW, HF, EB.
    - Treatments: 
      - Urea (U)
      - Urea with urease inhibitor (IU)
      - Ammonium nitrate (AN)
      - Control
    - Plot layout included subplots for NH3 emission measurements, soil sampling and N2O emission measurements, and biomass harvest.
  - 2017: Digestate experiment on winter wheat at NW and HF; additional grass trials at EB and HA.
    - Treatments: Digestate alone, Digestate + nitrification inhibitor (DMPP), acidified digestate, acidified digestate + DMPP, and Control.
    - Harvest and sampling subplots allocated for biomass, grain, and soil analyses.
  - 2018: UK-wide soil and biomass sampling across multiple land uses (revisiting some UGRASS-related sites).

- Meteorological and site data:
  - NW and HF: daily rainfall, daily temperature metrics; soil water-filled pore space (WFPS) via multiple soil moisture sensors.
  - EB: soil temperature and WFPS from handheld probes; long-term data from Easter Bush measurement station (air temp, soil temp, rainfall, 30-minute intervals).

- Protocols and data processing (WP-specific):
  - Sampling cadence differs between WP1 and WP2; crops harvested after a full growing season.
  - Sites used standardized sampling days within a site, with timing varying by weather and growth.
  - Crops harvested for yield and quality assessments; per-site units include dry matter yields and quality metrics (CP, ME, NDF/ADF, D-value, etc.).

- Data domains and key variables:
  - Yields and biomass (dry matter, acid detergent fibre, crude protein, metabolisable energy, fibre metrics, digestibility, etc.).
  - Nitrogen metrics:
    - Herbage/N crop N content (kg N ha-1), N offtake, nitrogen use efficiency (NUEc and NUEg) with explicit calculation formulas.
  - Greenhouse gases:
    - Ammonia (NH3) emission rates; nitrous oxide (N2O) fluxes; measurement methods include wind tunnels, passive samplers, static chambers, and isotopic analysis.
    - Temporal cumulatives via area-under-curve and Bayesian approaches for N2O.
  - Soil metrics (WP1 and WP2):
    - Inorganic N forms (NH4+, NO3-), amino acids, peptides, mineralisable N.
    - Dissolved organic carbon (DOC) and total dissolved N (TDN); DON as difference.
    - Microbial biomass C and N (MBC, MBN).
    - Physical/chemical soil properties: aggregate size distribution, texture (sand, silt, clay), soil moisture, soil organic matter (SOM), pH, electrical conductivity (EC).
    - Base cations (Na, K, Ca, Mg), total soil C and N, total P, POXC, extractable P pools (CE-citrate, acetic acid), Olsen-P.
    - DNA and nitrogen-cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC) via qPCR; microbial diversity indices (Shannon, richness) from amplicon sequencing (16S, ITS) and OTUs/ASVs.
    - Soil infiltration (infiltration rates) and water-release curves (HYPRO and related models).
  - Sampling and processing metadata:
    - Soil coring depths (0–15 cm, 15–30 cm, etc.), sampling dates, field plots, and lab QA/QC records.
    - Lab methods and instruments (colorimetry, ICP-OES, CHN analyzers, GC, HPLC, qPCR, sequencing pipelines) and data-handling workflows.
  - Data integration and analysis:
    - Data compiled in Excel; statistical and modeling analyses performed in R (including Bayesian modeling with JAGS for N2O; area-under-curve calculations; lognormal distributions for N2O flux).
    - QA/QC procedures with standard references and replicates; LIMS integration for certain analyses.

- Outputs, access, and references:
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Publications arising from CINAg datasets (examples provided).
  - Documentation and appendices detailing site-specific fertiliser rates, digestate protocols, and plot designs (A1–A3).

- GIS and data-integration considerations for mapping:
  - Geospatial layering of four farm platforms plus nine UK-wide sites with site- and plot-level attributes.
  - Multiscale datasets: field plots (subplots within plots) and plot grids, time-series data (2016–2018) for soil, gas fluxes, yields, and meteorology.
  - Variable-resolution data require harmonization of units, depths, and measurement techniques to enable spatial visualization of NUE indicators, NH3/N2O emissions hot spots, soil health metrics, and crop performance across sites.
  - Rich metadata supports geospatial analyses, reproducibility, and cross-site comparison of N-fertiliser and digestate strategies.