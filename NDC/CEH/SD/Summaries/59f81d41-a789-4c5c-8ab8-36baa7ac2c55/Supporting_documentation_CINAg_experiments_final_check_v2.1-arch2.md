# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose and scope
  - Aims to meet China-UK needs to optimise farm practices and soil management for more effective nitrogen use and reduced Nr losses to the environment.
  - Seeks holistic soil health metrics and real-time indicators of nitrogen use efficiency (NUE) to guide farm practices.
  - Plans translation of findings to Chinese farmers via the Science and Technology Backyard programme.

- Project objectives and structure
  - Develop novel indicators of NUE and combine with real-time physical/chemical metrics to inform soil health and management.
  - Test and develop on-field experiments and farm platforms to enable sustainable intensification.
  - Translate developments to farmers through established CAU/CAAS programmes.
  - Work packages (WPs):
    - WP1: Improved fundamental understanding of N cycling
    - WP2: Harnessing novel N technologies
    - WP3: Improved agronomic practices
    - WP4: Predictive capacity and knowledge exchange

- Participating organisations and locations
  - Core collaboration across UK and partner institutes (Centre for Ecology & Hydrology, Rothamsted Research, Bangor University, Bangor CEH, Edinburgh Napier University; multiple UK sites).
  - Four UK farm platforms (2016–2017): North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB).
  - 2018 UK-wide sampling conducted at nine sites with at least two land uses per site (Scotland, Wales, England).

- Experimental design and platforms
  - Inorganic fertiliser experiments (grass trials) in 2016 across NW, HF, EB; total N ~240 kg N ha-1; complete randomized block design with four fertiliser treatments (Urea; Urea + urease inhibitor IU; Ammonium nitrate AN; Control).
  - Digestate experiment (winter wheat) in 2017 at NW and HF; five digestate-related treatments (digestate; digestate + DMPP; acidified digestate; acidified digestate + DMPP; Control); complete randomized blocks; targeted N application rates around 190 kg N ha-1 (rates vary by plot).
  - 2017 EB/HA added grassland trials; site-specific layouts described in appendices.
  - UK-wide sampling (2018) across nine sites with diverse land uses for soil and biomass measurements.

- Meteorological and environmental data collection
  - NW and HF: daily rainfall, daily mean/min/max temperatures; soil water-filled pore space using soil moisture sensors.
  - EB: soil temperature and WFPS; long-term measurements at Easter Bush station (air temp, soil temp, rainfall at 30-min intervals).

- Measurements and outputs (key monitored variables)
  - Yields and biomass
    - Dry matter yields, forage quality metrics (crude protein, metabolisable energy, NDF/ADF, digestibility, etc.).
    - Harvest methods varied by site; standardization to area-based yields where possible.
  - Nitrogen content and NUE
    - Herbage N content and N offtake; NUEc (crop NUE) and NUEg (grain NUE) calculated from N offtake and N applied.
    - For 2016 grass trials, N content inferred from crude protein; for 2017 wheat, direct tissue/grain analysis.
  - Greenhouse gases
    - Ammonia (NH3) emissions: wind-tunnel measurements, acid traps, and dispersion-model-based estimates (FIDES) at EB for 2017 grass trial; cumulative NH3 emissions across N applications calculated.
    - N2O emissions: static chambers (manual and automatic) with isotopic analysis at HF; chamber-based flux calculations and Bayesian upscaling for cumulative flux.
  - Soil nitrogen metrics
    - Inorganic N metrics: NH4+, NO3-, amino acids/peptides, mineralisable N; sampling frequency tailored to WP1/WP2 timing.
  - Soil organic and mineral fractions
    - DOC, TDN; MBC, MBN; aggregate size distribution; soil texture; soil moisture; SOM (LOI).
  - Soil chemistry and fertility
    - pH, EC; base cations (Na, K, Ca, Mg); total soil C and N; total P.
    - Phosphorus pools: POXC; citric acid extractable P, acetic acid extractable P, Olsen-P.
  - Soil biology and genetics
    - DNA extractions; qPCR for nitrogen cycling genes (nifH, amoA for AOB/AOA, nirK/nirS, nosZ; ureC); OTUs and microbial diversity indices (16S rRNA, ITS sequencing); sequencing data processing.
  - Soil physical processes
    - Soil water infiltration (infiltration rates) and water release curves (HYPRO/ HYPRO-FIT analysis; bimodal soil water retention).
  - Biomass validation and land-use comparisons
    - Aboveground biomass measurements; exclusion cage methods for certain sites; moss growth assessment at Plynlimon; biomass per m2 estimates.

- Data protocols, processing, QA/QC and analytics
  - Distinct sampling protocols for WP1 and WP2; sampling days aligned within site, harvests planned per farm manager guidance.
  - Detailed methodological notes for each dataset (yields, NUE, NH3/N2O, soils, DNA, microbes, infiltration, hydraulic properties).
  - QA/QC across laboratories and methods; use of reference materials; replicates; cross-lab standard checks; LIMS-based data handling.
  - Data processing and analysis
    - Statistical analyses in R; use of area-under-curve for cumulative NH3 and N2O.
    - N2O flux modeling using Bayesian inference with MCMC (JAGS) to estimate emission dynamics and cumulative fluxes; parameter priors informed by literature (DNDC, Stehfest).
    - Nutrient calculations (N content, N offtake, NUE) standardized with defined equations; NUEc and NUEg consistently calculated across sites.
  - Data storage and dissemination
    - Datasets stored and uploaded to appropriate portals; project webpage for overview and access to datasets; publications linked to datasets.

- 2018 UK-wide sampling details
  - Nine sites across Scotland, Wales, England; multiple land uses per site (e.g., grazed pastures, arable, unimproved grassland, sown crops, peri-urban systems).
  - Biomass assessment via grazing exclusion where applicable; spring and late-summer/fall revisits; methodology for biomass estimation described.

- Appendices and supplementary material
  - Appendix A: detailed fertiliser application rates, dates, and harvests for 2016 inorganic fertiliser trials (HF, NW) and 2016 EB; 2017 digestate pre-treatment and plot designs.
  - Additional figures and tables detailing plot layouts, sampling dates, and site-specific information.

- Key references and resources
  - Project page: www.rothamsted.ac.uk/international/china/cinag
  - Selected publications resulting from the dataset (e.g., assessments of N fertilisers, digestate processing, and nitrogen dynamics).

- Relevance for environmental monitoring and policy evaluation
  - Provides a comprehensive, multi-site data framework for monitoring N cycling, NUE, and Nr losses under different fertiliser regimes and digestate applications.
  - Emphasizes standardized data collection, quality assurance, cross-site comparability, and robust statistical approaches to quantify emissions and soil health indicators.
  - Aims to deliver interpretable outputs (yields, NUE metrics, emissions, soil health indicators, and biodiversity metrics) in formats suitable for reports, maps, and policy performance assessment, with underlying datasets accessible for scrutiny and reuse.