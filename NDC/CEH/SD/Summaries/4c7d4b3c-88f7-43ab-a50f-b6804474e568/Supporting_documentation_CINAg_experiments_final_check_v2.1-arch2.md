# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Aims and scope
  - Use data to consistently demonstrate environmental condition and nitrogen management performance over time.
  - Develop indicators of nitrogen use efficiency (NUE) and holistic soil health metrics to inform farm practices and policy.
  - Test on-field experiments and farm platforms to enable sustainable intensification.
  - Translate developments to Chinese farmers via the Science and Technology Backyard program.

- Project structure (work packages)
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

- What the project is about
  - CINAg aims to optimise farm practices and soil management to enhance NUE and reduce nitrogen losses to the environment.
  - Objectives include: new NUE indicators combined with real-time soil metrics; field experiments and farm platforms; knowledge transfer to farmers in China.
  - Outputs include standardized data and protocols to support policy and practice.

- Locations and experimental platforms
  - Four UK farm platforms (across England, Wales, Scotland): North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB).
  - 2016–2017 experiments
    - 2016: inorganic fertiliser trials on grass across NW, HF, EB (complete randomized blocks; 4 treatments: Urea; Urea + inhibitor; AN; Control).
    - 2017: digestate trial on winter wheat at NW and HF; additional grass trials at EB and HA.
  - 2018: nine UK-wide soil sampling sites with at least two land uses per site.
  - Site characteristics include soil type, texture, mean annual temperature, and precipitation (Tables provided in the report).

- Meteorological data
  - NW and HF: daily rainfall and temperature data from on-site weather stations.
  - EB: soil temperature and soil water-filled pore space; long-term data from a permanent measurement station.
  - Overall: meteorological context used in interpretation of GHG fluxes and nutrient dynamics.

- Experimental information and design
  - 2016 inorganic fertiliser experiments (grass): complete randomized blocks with four treatments and phosphorus, potassium, sulfur applied as per guidelines; multi-subplot layout for NH3, soil sampling/N2O, and biomass harvest.
  - 2017 digestate experiment (winter wheat): complete randomized blocks with five digestate treatments and controls; harvest and sampling subplots; digestate application rates around 190 kg N ha-1 (rates varied in-field).
  - 2018 UK-wide sampling: field sites with differing land uses; grazing exclusion cores used to estimate biomass in active grazing sites; moss mesh at some sites for bryophyte growth assessment.

- Protocols and data processing
  - Clear separation of sampling protocols by WP1 and WP2; harvests aligned with growing seasons and farm manager guidance.
  - Yields and biomass
    - Grass yields (dry matter, quality metrics like CP, ME, crude fibre, NDF, ADF, digestibility) and harvest methods varied by site.
    - Wheat yields (grain and straw) and grain quality metrics; methods to convert to per-hectare basis.
  - N content, N offtake, NUE
    - Grass N content derived from crude protein using a standard conversion; N offtake calculated from yield and N content; NUEc and NUEg computed using treated vs. control plots.
    - Wheat N content and total crop N used to compute NUE similarly.
  - GH gases: ammonia and nitrous oxide
    - NH3 emissions: wind tunnels at NW and HF; sampling frequency varied by treatment; acid traps analyzed colorimetrically or by equivalent methods.
    - N2O emissions: static chambers (manual and/or automatic) with gas analysis (GC or isotopic analyser); fluxes calculated per chamber, with cumulative fluxes derived via area under the curve or Bayesian methods where applicable.
    - For EB grass trial (2017): N2O fluxes measured with PVC chambers and analyzed with GC; cumulative fluxes modeled using Bayesian methods (MCMC in JAGS) to capture temporal dynamics.
  - Soil sampling and metrics (WP1 and WP2)
    - Topsoil cores (0–15 cm) and deeper depths; sampling dates aligned to fertilisation and harvests.
    - Soil N metrics: NH4+, NO3-, amino acids, peptides, mineralizable N; extraction with KCl; colorimetric methods and fluorometric analyses.
    - DOC and TDN measured in K2SO4 extract supernatants.
    - Microbial biomass C and N (MBC/MBN) via chloroform fumigation methods.
    - Physical and chemical soil properties: aggregate size distribution, texture (sand/silt/clay), soil moisture, SOM (loss on ignition), pH, EC, base cations (Na, K, Ca, Mg).
    - Total C and N via Elemental analyses; total P via H2O2/H2SO4 digestion and colorimetric measurement; POXC as a soil quality proxy.
    - Phosphorus pools: citric acid extractable P, acetic acid extractable P, Olsen-P; method details for each.
  - DNA and microbial functional potential (5.4.13–5.4.14)
    - DNA extraction from soil; qPCR targets for nitrogen cycling genes (nifH, amoA AOA/AOB, nirK, nirS, nosZ I/II, ureC); 16S rRNA and ITS amplicon sequencing for bacterial and fungal communities.
    - Amplicon sequencing on Illumina MiSeq; data processing with in-house and standard pipelines; diversity metrics (Shannon, richness) and OTU-level analyses.
  - Soil infiltration and water release
    - Infiltration: Mini Disk Infiltrometer at multiple tensions; hydraulic conductivity derived.
    - Water release curves: hyprop and WP4 for low and high suction ranges; Mualem-Durner models used to fit curves.
  - Data management and QA/QC
    - QA/QC with laboratory standards (BS1, BS3), blanks, random replicates; instrument calibration and cross-lab checks.
    - Data compiled in Microsoft Excel; quality checks by multiple staff before release.
  - Data processing and modeling
    - WP1 vs WP2 sampling timelines; normalization of N content to dry matter; NUE calculations.
    - N2O cumulative flux estimation via area under the curve; Bayesian inference for flux dynamics using MCMC (JAGS) with informed priors from literature.
    - Data analysis conducted in R (various versions) with standard statistical practices.

- Outputs, data portals, and publications
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Publications (2018) deriving from these datasets include:
    - Assessing the benefits and wider costs of different N fertilisers for grassland agriculture.
    - Advanced processing of food waste-based digestate for mitigating nitrogen losses in a winter wheat crop.
  - Datasets and methodologies are designed to support sharing via appropriate portals and to inform broader environmental monitoring and policy assessment.

- Particular challenges highlighted for Analysts Monitoring the Environment
  - Increasing the value of monitoring datasets by integrating them with other relevant datasets (beyond single-use applications).
  - Enabling broad access to the underlying data used to produce outputs, improving transparency and scrutiny of environmental health and policy performance.