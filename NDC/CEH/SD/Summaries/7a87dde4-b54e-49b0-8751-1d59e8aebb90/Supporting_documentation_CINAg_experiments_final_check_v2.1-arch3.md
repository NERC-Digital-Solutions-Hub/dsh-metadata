# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Overview
  - CINAg project aims to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses.
  - Objectives: develop novel NUE indicators and holistic soil-health metrics; test in-field experiments and farm platforms; translate findings to Chinese farmers via Science and Technology Backyard.
  - Structure: four work packages
    - WP1: Improved fundamental understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange

- Study sites and monitoring framework
  - Four UK farm platforms (cross-UK experiments): North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB).
  - 2016–2017: inorganic fertiliser trials on grass; 2017: digestate trial on winter wheat; 2017–2018: additional grass trials; 2018 UK-wide soil sampling across nine sites with multiple land uses.
  - Site information includes soil types, textures, mean annual temperature, and precipitation; detailed coordinates and field layouts are provided.
  - Meteorological data collection includes daily rainfall and temperature at several sites; soil temperature and soil moisture sensors deployed at multiple depths.

- Experimental design and treatments
  - Inorganic fertiliser experiments (grass, 2016; EB also in 2017)
    - Treatments: Control, Urea (U), Urea + urease inhibitor (IU), Ammonium-nitrate (AN)
    - Complete randomized blocks; three subplots per plot for NH3, N2O measurements, and biomass/yield/quality assessments
    - Total N application around 240 kg N ha-1 across treatments
  - Digestate experiment (winter wheat, 2017)
    - Treatments: Digestate; Digestate + nitrification inhibitor (DMPP); acidified digestate; acidified digestate + DMPP; Control
    - Randomized blocks; harvest and sampling subplots; target 190 kg N ha-1 as digestate
  - UK-wide sampling (2018)
    - Land uses across sites include grazed, arable, permanent grass, etc.; biomass measurements conducted; sampling days adjusted for weather and peak biomass

- Protocols and data processing (WP-specific)
  - Yields and biomass (5.1)
    - Dry matter yields and forage quality metrics (CP, ME, MAD, NDF/ADF, D value, TGW)
    - Site-specific harvest procedures; sub-sampling and NIR-based analysis for quality
  - Wheat N content, N offtake and NUE (5.2)
    - N content derived from crude protein (factor 6.25) or direct analyses
    - N offtake from grain and straw; NUEc and NUEg calculations
  - Greenhouse gases: Ammonia (NH3) and N2O (5.3)
    - NH3: wind tunnels with acid traps; cumulative emissions via area-under-curve; different measurement protocols by site
    - N2O: manual and automatic chambers; gas analysis by GC or Isotopic Analyser; cumulative emissions modeled via time-series and Bayesian methods
    - For digestate, N loss expressed as a percentage of applied N
    - NH3 and N2O temporal dynamics modeled with lognormal frameworks; Bayesian estimation (MCMC via JAGS)
  - Soil sampling and analyses (5.4)
    - WP1: 0–15 cm topsoil cores; WP2: intensive post-application soil sampling schedules
    - Nitrogen metrics: NH4+, NO3-, amino acids, peptides, mineralisable N
    - DOC and TDN; DON by difference
    - Microbial and genetic metrics: MBC, MBN; DNA extractions; qPCR targets for nifH, amoA, nirK, nirS, nosZ (clades I & II), ureC
    - Microbial diversity: 16S rRNA and ITS amplicon sequencing; diversity indices (Shannon, richness)
    - Soil physics/chemistry: aggregate-size distribution; texture (sand/silt/clay); soil moisture and SOM (LOI); pH and EC; base cations (Na, K, Ca, Mg); total C and N; total P
    - P pools: total P; citric acid extractable P; acetic acid extractable P; Olsen-P (in WP1 and WP2)
    - POXC (permanganate oxidisable C)
    - Infiltration and water retention: soil infiltration (Mini Disk Infiltrometer), water release curves (HYPROP, WP4), hydraulic parameters (Mualem-Durner model)
    - QA/QC: use of reference standards, replicates, and data checks; LIMS and Excel-based data compilation
  - Data governance and dissemination
    - Data are compiled and shared through project outputs; references and project webpage provided
    - Publications arising from CINAg datasets include assessments of fertiliser types and nitrogen losses, and digestate processing for mitigating nitrogen losses

- Data management, challenges, and governance (alignment with monitoring-framework archetype)
  - Data sourcing and integrity
    - Multi-site data collection with standardized yet site-adapted protocols
    - Metadata gaps and transformation requirements acknowledged; ongoing data verification with originators
  - Data sharing and openness
    - Public sharing of underlying data is pursued but can pose barriers; governance processes required to ensure openness
  - Data gaps and silos
    - Across sites and work packages, potential data gaps and organisational silos noted; cross-site coordination is essential
  - Data quality assurance
    - Rigorous QA/QC protocols across chemical, physical, and molecular measurements; use of standards and cross-lab QA
  - Communication of complex results
    - Aims to translate complex nitrogen dynamics into actionable indicators for farm management and policy

- Outputs and references
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Key publications and datasets cited, including assessments of fertilisers and digestate processing
  - Appendix and supplementary tables/figures document detailed methods, site layouts, and protocol specifics

- Enduring relevance for monitoring and policy
  - Provides a comprehensive suite of indicators for N cycling, NUE, soil health, and environmental losses (NH3 and N2O)
  - Demonstrates cross-site monitoring frameworks (field platforms and UK-wide sampling) suitable for evaluating policy changes in fertiliser use and substrate management
  - Illustrates advanced data processing (Bayesian modeling, time-series upscaling) and rigorous QA/QC applicable to environmental monitoring frameworks