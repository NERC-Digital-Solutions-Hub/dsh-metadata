# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose and scope
  - CINAg project aims to optimise farm practices and soil management to use nitrogen sources efficiently and reduce environmental Nr losses, addressing both China and the UK.
  - Objectives: develop novel indicators of nitrogen use efficiency (NUE) linked to holistic soil health metrics; test and translate findings into field practices and farmer outreach through the Science and Technology Backyard programme.
  - Structure: four work packages
    - WP1: Improved fundamental understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange

- Key sites and experimental design
  - Four farm platforms across the UK (2016–2017): North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB)
    - Treatments included inorganic fertilizers (urea, urea with urease inhibitor IU, ammonium nitrate) and a grass/balanced control; 3 subplots per plot for NH3 flux, N2O flux, and biomass/yield sampling.
    - Digestate experiments (2017) at NW and HF with five digestate-related treatments (including digestate alone, acidified digestate, with nitrification inhibitor, and a control).
  - 2018 UK-wide sampling at nine sites with multiple land uses to capture broader soil and vegetation variability.

- Data collected and main variables
  - Agronomic outcomes
    - Yields and biomass; herbage quality metrics (crude protein, metabolisable energy, fibre fractions, ash, D value, etc.); yields reported as dry matter (t/ha) and related quality parameters.
    - Nitrogen content and uptake in herbage and grain/straw (N content kg N ha-1; NUEc and NUEg calculated from crop N uptake and applied N).
  - Soil and nutrient metrics (WP1 and WP2)
    - Inorganic N forms: NH4+, NO3-; mineralisable N; amino acids and peptides; DOC and TDN; DON corrections.
    - Soil organic and physical properties: soil moisture, SOM (LOI), texture (sand/silt/clay), aggregate size distribution, pH, EC, base cations (Na, K, Ca, Mg), total C and N, total P, POXC, Olsen P, citric acid and acetic acid extractable P.
    - Microbial and molecular data: DNA extraction; qPCR targets for nitrogen cycling genes (nifH, amoA for AOB/AOA, nirK/nirS, nosZ I/II, ureC); OTUs and microbial diversity (16S rRNA and ITS amplicon sequencing); microbial biomass C and N (MBC/MBN); microbial diversity indices (Shannon, richness).
  - Gaseous emissions and fluxes
    - Ammonia (NH3) emissions via wind tunnel measurements (flux in μg NH3-N m-2 s-1) and dispersion/diffusion modelling at EB.
    - Nitrous oxide (N2O) emissions via static manual and automatic chambers (flux in μg N2O-N m-2 h-1); cumulative fluxes computed for post-fertilisation periods.
  - Meteorological and site data
    - Daily rainfall and temperatures at NW, HF; soil temperature and water-filled pore space; long-term met data at Easter Bush measurement station.
  - Soil functional and process metrics
    - Infiltration (mini-disk infiltrometer; hydraulic conductivity) and soil water release curves (HYPRO-FIT bimodal retention model; Mualem-Durner concepts).

- Protocols, data processing, and analysis
  - Experimental protocols
    - WP1 measurements: baseline soil sampling before treatments, repeated sampling around key growth stages; soil cores (0–15 cm, 15–30 cm, below 30 cm) for multiple parameters.
    - WP2 measurements: intensive soil sampling following N fertiliser/digestate applications with frequent sampling early on, then weekly/monthly; targeted plots for NH3/NH4+/NO3- analyses.
  - Yields and quality analyses
    - Harvest strategies varied by site; subsamples analyzed for quality metrics (CP, ME, fibre, etc.) using NIR or standard lab methods.
  - NUE calculations
    - NUEc = (Nt - Nc) / Napplied × 100; NUEg similarly for grain and straw N offtake, using measured N content and yields.
  - Gas emissions and data processing
    - NH3: fluxes from wind tunnels used to compute cumulative NH3 losses; for EB, NH3 fluxes derived through a dispersion model (FIDES) with concentration measurements from passive samplers.
    - N2O: manual/automatic chamber measurements; cumulative fluxes derived via area-under-curve methods or Bayesian approaches depending on site; for EB, N2O fluxes treated with a Bayesian lognormal framework to obtain cumulative flux distributions.
  - Statistical and data handling
    - Data compiled in Excel; R used for analysis; JAGS (Bayesian) used for N2O flux modeling; QA/QC procedures embedded across labs and instruments.
  - Timeframe and sampling cadence
    - WP1: pre-treatment baselines, subsequent harvest-time sampling; 2016–2017 core experiments; 2018 broad UK sampling.
    - WP2: post-application intensive sampling schedules defined per site and per treatment.

- Data management, QA/QC, and accessibility
  - Laboratories and partners: Bangor University, CEH Bangor, CEH Lancaster, Rothamsted Research (HA, NW), and Rothamsted Harpenden; DNA/qPCR and sequencing conducted at CEH walls/Harpenden with external labs for some steps.
  - QA/QC highlights: use of standard reference materials (BS1/BS3), random replicates, lab standards, calibration curves, and cross-site standardization; data checked by multiple staff before release.
  - Data formats and availability
    - Datasets exist in structured lab reports and Excel sheets; analysis pipelines use R and JAGS; project page links and publications provide access to published results and data descriptions.

- Outputs and references
  - Publications stemming from these datasets include assessments of different nitrogen fertilisers for grassland and advanced digestate processing for N-loss mitigation.
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Notable outputs include methodological papers detailing NUE indicators, NH3/N2O measurement approaches, and soil N cycling analyses.

- Practical considerations for data support
  - Data integration across sites requires harmonised metadata (locations, soil types, management histories, and measurement protocols) and consistent units.
  - Complex treatment structures (inorganic N forms, inhibitors, digestate variants) necessitate robust data lineage tracking and clear data dictionaries.
  - Advanced analyses (N2O/NH3 fluxes, Bayesian modeling) rely on reproducible scripts (R, JAGS) and well-documented parameter priors and assumptions.