# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose and scope
  - Documents the CINAg project data and supporting methods to optimise farm practices and soil management for more effective nitrogen (N) use and reduced Nr losses.
  - Structured to support cross-UK and China collaboration with four work packages: 
    - WP1: Improved fundamental understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange
  - Aims to translate developments to Chinese farmers via Science and Technology Backyard programmes.

- Data assets and study sites
  - Four UK farm platforms (2016–2017): 
    - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
  - Experiments
    - 2016 inorganic fertiliser trials on grassland (NW, HF, EB)
    - 2017 digestate trial on winter wheat (NW, HF)
    - 2017 additional grassland trials at EB and HA
  - 2018 UK-wide soil sampling across nine sites with at least two land uses per site
  - Site characteristics include soil types, textures, mean annual temperatures, and precipitation
  - Data and sites are linked to published works and a project webpage

- Experimental design and data collection scope
  - Inorganic fertiliser experiments (grass trials, 2016; EB 2016 added)
    - Complete randomized block design; four fertiliser treatments plus controls
    - Treatments: Urea (U), Urea with urease inhibitor (IU), Ammonium nitrate (AN), Control
    - Total N = 240 kg N ha-1 across plots; sub-plots for NH3 emissions, N2O emissions, and harvest yields
  - Digestate experiment (winter wheat, 2017)
    - Complete randomized block design; five digestate treatments including with nitrification inhibitor (DMPP) and acidified digestate, plus control
    - Target N applied as digestate ~190 kg N ha-1 (actual rates varied)
    - Harvest sub-plots for biomass and grain; additional sampling sub-plots for analysis
  - UK-wide sampling (2018)
    - Nine sites with diverse land uses and soil types; biomass and soil measurements across land uses
  - Experimental layouts and field protocols are documented in appendices and site-specific tables

- Measurements and data domains
  - Yields and biomass
    - Dry matter yields, quality metrics (crude protein, ME, fibre, N content), digestibility, metabolizable energy
  - Nitrogen content and use
    - Grass N content, N offtake, nitrogen use efficiency (NUEc, NUEg)
    - N content derived from crude protein or direct tissue analyses; calculations for N offtake and NUE
  - Greenhouse gases
    - Ammonia (NH3) emissions via wind tunnels and acid traps; N2O emissions via manual and automatic chambers
    - Flux calculations and cumulative emissions with site-specific methods
  - Soil sampling and metrics (WP1 and WP2)
    - Topsoil 0–15 cm and deeper cores; NH4+, NO3-, mineral N pools; amino acids and peptides; mineralisable N
    - Dissolved organic C (DOC) and dissolved total N (TDN); DON derived by difference
    - Microbial biology: microbial biomass C and N (MBC/MBN); DNA-based metrics; OTUs and diversity indices
    - Soil physical properties: aggregate size distribution, texture (sand/silt/clay), soil moisture, SOM
    - Soil chemical properties: pH, electrical conductivity (EC), base cations (Na, K, Ca, Mg)
    - Total soil C and N; total phosphorus (P)
    - POXC (permanganate oxidisable C) and extractable P fractions (CEH-Bangor and Olsen-P; acetic acid extractable P for WP2)
  - Biological and molecular analyses
    - DNA extraction and qPCR for nitrogen-cycling genes (nifH, amoA for AOA/AOB, nirK, nirS, nosZ, ureC)
    - 16S rRNA (bacteria/archaea) and ITS (fungi) amplicon sequencing; diversity indices (Shannon, richness)
    - Sequencing data processed with established pipelines; QA/QC with standards and controls
  - Hydrology and soil physics
    - Soil infiltration (mini-disk infiltrometer) and soil water release curves; HYPRO-FIT modeling for retention curves

- Protocols, data processing and QA/QC
  - Distinct protocols for WP1 (soil and biomass metrics pre- and post-treatment) and WP2 (in-field sampling cadence and lab analyses)
  - Data collection across sites performed on or near the same days within a site; harvest timing aligned with crop peak biomass
  - Analytical methods and units standardized where possible (e.g., N content conversions, NUE calculations)
  - QA/QC measures include laboratory standards, random replicates, and cross-lab checks; data validated before release
  - Data processing tools and environments
    - Excel-based data compilation (primary)
    - LIMS for some workflows
    - Statistical analyses in R (versions 3.2.x–3.3.x)
    - Bayesian inference for N2O flux estimation via JAGS
    - Specialized software for image/biomass and sequencing pipelines
  - Data documentation and traceability
    - Appendices with detailed tables (A1–A3) for treatments, dates, and harvests
    - Protocol separation and clear delineation ofWP1 vs WP2 measurements
    - Data references and project outputs linked to peer-reviewed publications

- Data governance, sharing, and dissemination
  - Data management emphasizes standardisation across sites and systems to ensure interoperability
  - Datasets are intended to be uploaded to relevant portals and catalogues; machine-readable datasets with clear metadata
  - Publications derived from the data are cited (e.g., Carswell et al. 2018; Sánchez-Rodríguez et al. 2018)
  - Project webpage and data products support wider dissemination and reuse

- Documentation of lines of responsibility and collaboration
  - Core project team and contributing institutions across the UK (Centre for Ecology & Hydrology, Rothamsted Research, Bangor University, Edinburgh Napier University)
  - Explicit lab roles for each measurement stream (e.g., NH3/N2O measurements, soil chemistry, microbial genetics) and cross-site QA oversight
  - Data provenance includes site names, coordinates, soil types, plots, treatments, sampling dates, and analysis methods

- Challenges and considerations for Data Stewards
  - Heterogeneity of systems, formats, and measurement techniques across sites and years
  - Ensuring timely data submission and complete metadata to enable cross-site integration
  - Managing large, multi-domain datasets (soil chemistry, gas fluxes, biomass, genomics, etc.)
  - Maintaining data discoverability and usability through consistent metadata, versioning, and documentation
  - Aligning data with user needs for interpretable NUE indicators, soil health metrics, and translatability to farm practices
  - Ensuring update mechanisms and governance for ongoing data streams and future extensions

- Appendices and references
  - Appendices include detailed site-specific data, fertilizer and digestate treatment schedules, and methodological specifics
  - References document established methods and prior work underpinning measurement techniques and analysis approaches

- Notable outputs and workflow summary
  - Datasets span field experiments, lab analytics, and advanced molecular analyses
  - Data flow from field sampling to lab assays, to data processing in Excel/R/LIMS, to statistical modelling (e.g., NUE calculations, N2O Bayesian flux estimates)
  - Results support evaluation of different N fertilisers and digestates for grassland and cereal systems, with implications for sustainable nitrogen management and environmental impact mitigation

- Project context and access
  - Public-facing materials include a project webpage and two peer-reviewed publications
  - Data governance considerations are aligned with ensuring datasets are ready for discovery, reuse, and integration into predictive knowledge platforms for agronomic decision-making