# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose: Document data collection, processing, and analysis framework for CINAg, an international project to optimise farm practices and soil management for better nitrogen use efficiency (NUE) and reduced environmental Nr losses, with knowledge transfer to Chinese farmers via the Science and Technology Backyard programme.

- Aims and structure
  - Develop novel NUE indicators and holistic soil-health metrics using real-time physical/chemical data.
  - Test and develop field experiments and farm platforms for sustainable intensification.
  - Translate developments to farmers in China.
  - Work packages: WP1 (fundamental N cycling), WP2 (novel N technologies), WP3 (improved agronomic practices), WP4 (predictive capacity and knowledge exchange).

- Core team and institutions
  - Core group across UK institutions: Centre for Ecology & Hydrology (CEH), Rothamsted Research, Bangor University, Bangor (North Wales), Easter Bush (Edinburgh), and partner universities.
  - New addresses for collaborators in Spain and the UK.

- Study sites and platforms
  - Four UK farm platforms (2016–2017) for fertiliser experiments:
    - North Wyke (NW) – Rothamsted/CEH, Devon
    - Harpenden (HA) – Rothamsted
    - Henfaes Farm (HF) – Bangor University, North Wales
    - Easter Bush (EB) – CEH, Edinburgh
  - 2018 UK-wide soil sampling across nine sites with at least two land uses per site.
  - Site characteristics include soil type, texture, mean annual temperature, and precipitation.

- Data types and measurements
  - Yields and biomass
    - Grass yields (dry matter), quality metrics (crude protein, ME, NDF/ADF, etc.); digestibility (D value).
    - Winter wheat yields (grain and straw), moisture, and grain quality metrics.
  - Plant N content and use
    - Herbage N content, N offtake, nitrogen-use efficiency (NUEc and NUEg).
  - Greenhouse gases
    - Ammonia (NH3) emissions via wind-tunnel measurements and passive samplers; nitrous oxide (N2O) fluxes via static chambers (manual and automatic) and isotopic analyses.
    - Emissions expressed as fluxes per area and cumulative emissions; temporal dynamics modeled (lognormal approach with Bayesian/MCMC estimation).
  - Soil sampling and metrics (WP1 and WP2)
    - Nitrogen metrics: NH4+, NO3−, amino acids, peptides, mineralisable N.
    - Dissolved organic carbon and nitrogen (DOC/TDN).
    - Microbial biomass C and N (MBC/MBN); DNA, qPCR targets for nitrogen-cycling genes; OTUs and diversity indices.
    - Physical/chemical soil properties: aggregate size distribution, texture, soil moisture, soil organic matter (LOI), pH, EC, base cations (Na, K, Ca, Mg), total C and N, total P, POXC, citrate/acetic-acid extractable P, Olsen-P.
    - Soil nutrients and processes: inorganic N pools, DON, mineralisable N, soil N metrics over time.
    - Soil microbial community analyses: 16S rRNA (bacteria/archaea), ITS (fungi); nifH, amoA (AOA/AOB), nirK/nirS, nosZ, ureC genes; diversity metrics and qPCR results.
    - Soil hydraulic properties: water infiltration (infiltration tests), water release curves (HYPRO/Hyprop), Mualem–Durner modeling parameters.
  - Meteorology
    - Site-specific weather data (rainfall, air/soil temperatures) and soil moisture sensors; long-term data from measurement stations (EB) and field sensors at HF/NW.
  - Sampling protocols and timing
    - WP1: baseline and harvest-time soil cores (0–15 cm, then deeper samples); repeated sampling around fertiliser events.
    - WP2: intensive soil sampling after digestate/fertilisers (frequent early-season sampling, then monthly/seasonal).
  - Data management
    - Data captured in Microsoft Excel; Lab analyses governed by standard methods; QA/QC using reference standards (BS1/BS3), replicates, and cross-lab validation.
    - Data integration supported by LIMS (Batch97) and analysis in R, Bayesian tools (JAGS), and standard statistical procedures.

- Experimental design and protocols
  - Inorganic fertiliser experiments (grass trials, 2016; EB 2017 added)
    - Complete randomized block design; treatments: Urea (U), Urea with urease inhibitor (IU), Ammonium-nitrate (AN), and Control.
    - Uniform P, K, S fertilisation per Defra guidelines; plots subdivided for NH3, N2O measurements, and biomass/yield assessment.
  - Digestate experiments (winter wheat, 2017)
    - Complete randomized block design; treatments: Digestate; Digestate + DMPP (nitrification inhibitor); Acidified digestate; Acidified digestate + DMPP; Control.
    - Harvest plots subdivided for biomass and sampling; N application rate targeted at 190 kg N/ha from digestate with field adjustments.
  - UK-wide sampling (2018)
    - Nine sites with diverse land uses; biomass measurements collected; grazing exclusion cages used where applicable to estimate production.

- Data processing, analysis, and reporting
  - Yields and NUE calculations
    - NUEc and NUEg formulas using crop N offtake, control means, and applied N.
  - Gas flux calculations
    - NH3: flux from wind-tunnel measurements using concentration differentials and airflow; N losses expressed as percent of applied N for digestate trials; cumulative NH3 via area-under-curve approaches.
    - N2O: manual/automatic chamber flux calculations; cumulative flux via area-under-curve and Bayesian time-series models; flux distributions modeled as lognormal; MCMC (JAGS) used for parameter estimation.
  - Soil and plant analyses
    - Standard chemical assays for NH4+/NO3−, DON/DOC, minerals; colorimetric methods for P; spectrophotometric measurements; LC/ICP-OES for cations; total C/N analyses via elemental analyzers; PoXC via permanganate oxidation.
    - N genes and OTUs: qPCR targets for nitrogen-cycling genes; amplicon sequencing (16S rRNA and ITS); rarefaction and diversity analyses (Shannon, richness); taxonomic assignment (Greengenes, UNITE) with R vegan tools.
  - Soil properties and hydraulics
    - Texture by laser diffraction; aggregate size distribution; soil moisture and SOM content by LOI; pH/EC by standard methods; base cations by ammonium acetate extraction; total P by digestion and colorimetric analysis; POXC by KMnO4 method.
    - Infiltration and water-release curves analyzed with HYPRO-FIT and bimodal soil retention models (Durner/Peters).
  - Data integration and quality checks
    - QA/QC protocols for laboratory analyses; cross-lab comparisons; calibration with standards; data checks by multiple staff prior to release.
    - Use of public project web page and linked publications for disseminating datasets and results.
  - Outputs and dissemination
    - Project webpage: www.rothamsted.ac.uk/international/china/cinag
    - Publications arising from the datasets (examples provided).

- Data management, access, and challenges
  - Data management tools include LIMS (Batch97), Excel-based datasets, and R-based analyses; collaboration across multiple labs and sites requires careful harmonisation of protocols and units.
  - Key challenges highlighted
    - Time spent understanding the ask and aligning data across diverse teams.
    - Patchy data and heterogeneity across site formats and measurement regimes.
    - Accessing data from different systems and communicating complex results simply.
    - Ensuring outputs are widely shared and reused, and promoting outputs to end users.

- End goals and practical relevance
  - Generate robust, real-time-like indicators of soil health and NUE to guide farm practices and policy.
  - Build predictive capacity and knowledge exchange to support sustainable nitrogen management across UK and China.
  - Deliver insights and tools that support self-serve data exploration for end users and inform broader agricultural policy and practice.