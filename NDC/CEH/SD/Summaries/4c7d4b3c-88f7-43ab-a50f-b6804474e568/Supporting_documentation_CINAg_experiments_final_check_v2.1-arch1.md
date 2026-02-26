# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- The document describes the CINAg project’s data and experimental framework to optimise farm practices and soil management for nitrogen use efficiency (NUE) and to mitigate environmental Nr losses.
- It integrates multi-site UK experiments (grassland and winter wheat), farm-scale platforms, UK-wide soil sampling, and extensive soil- and plant-related measurements.
- Datasets underpin development of novel NUE indicators, real-time soil-health metrics, and field-tested practices, with translation to Chinese farming communities through established programmes.

## 1. Project aims and structure

- Primary aims
  - Develop novel indicators of N use efficiency (NUE) combined with real-time physical/chemical soil metrics to form holistic soil-health indicators that guide practice.
  - Use these indicators to test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers via the Science and Technology Backyard programme.
- Work packages (WPs)
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## 2. Experimental platforms and UK-wide sites

- Four UK farm platforms (2016–2017)
  - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
  - Worksheets summarize site coordinates and fertiliser experiments per site; soil types and climates are described.
- 2018 UK-wide soil sampling
  - Nine sites across Scotland, Wales, England with two or more land uses per site (Table 3).
  - Sites include Parsonage Down, Silwood, Harpenden, Wymondham, Plynlimon, Abergwyngregyn, Newborough, Easter Bush, Kirkton.
  - Objective: broad soil and aboveground biomass measurements across diverse land uses.
- Meteorological data
  - NW and HF: daily rainfall, temperature; soil moisture sensors (2.5 cm depth) for water-filled pore space (WFPS)
  - EB: handheld weather instruments; a long-term measurement station at Engineer's Field (temp, rainfall, etc.)
  - Data support interpretation of gas fluxes and nutrient cycling

## 3. Experimental information

- 2016 inorganic fertiliser experiments (grass trials)
  - Sites: NW, HF, EB
  - Design: complete randomized blocks (EB had four control plots with four replicates per treatment)
  - Treatments per plot
    - Urea (U)
    - Urea with inhibitor (IU)
    - Ammonium-nitrate (AN)
    - Control
  - Total monitored N: 240 kg N ha−1 across plots
  - Sub-plot structure (NW and HF): NH3 emission sub-plot, N2O emission/soil sampling sub-plot, biomass harvest sub-plot
  - EB 2016 layout varied; management followed standard silage rotations
- 2017 digestate experiment (winter wheat)
  - Sites: NW and HF; EB and HA had additional grassland trials
  - Design: complete randomized blocks; five replicates per digestate treatment
  - Treatments
    - Digestate only
    - Digestate + nitrification inhibitor (DMPP)
    - Acidified digestate
    - Acidified digestate + DMPP
    - Control
  - Target N application: 190 kg N ha−1 as digestate (rates varied in-field)
  - Plot layout: harvest and sampling subplots; digestate banding at NW (proportional sampling at HF)
- 2018 UK-wide sampling
  - Re-visits sites from UGRASS project; measurement of aboveground biomass and soil metrics across land uses

## 4. Protocols and data processing

- Sampling and timing
  - WP1 and WP2 sampling schedules differ; all plots sampled on the same day within a site; harvest timing aligned with peak biomass
- Yields and biomass (5.1)
  - Measures: dry matter yields, forage quality metrics (Crude Protein, ME, NDF, ADF, etc.)
  - Grass trials: multiple cuts; harvester methods; lab analyses (NIR)
  - Wheat: grain and straw yields; moisture; TGW; standard NUE calculations
- N content, N offtake, NUE (5.2)
  - NW/HF 2016: grass N content from crude protein (factor 6.25); N offtake calculated from yield and N content
  - 2017: grain and straw from harvest; total N analysed; NUEc and NUEg calculated with Fungible equations
  - EB: total crop N analysed; NUE calculated similarly
- Greenhouse gas sampling (5.3)
  - Ammonia (NH3): wind tunnels or passive samplers; concentration-based flux calculations; area under the curve (AUC) for Cumulative NH3
  - Nitrous oxide (N2O): manual and automated chambers; flux calculations; cumulative emissions via AUC and Bayesian approaches
  - Digestate 2017: N-loss expressed as percentage of total N applied
- Soil sampling and metrics (5.4)
  - 5.4.1 Soil N metrics: NH4+, NO3−, amino acids/peptides, mineralisable N
  - 5.4.2 DOC and TDN; DON estimation
  - 5.4.3 Microbial biomass C and N (MBC/MBN)
  - 5.4.4 Aggregate size distribution
  - 5.4.5 Soil texture (sand, silt, clay)
  - 5.4.6 Soil moisture and SOM (loss-on-ignition)
  - 5.4.7 pH and EC (WP1 and WP2, different methods)
  - 5.4.8 Base cations (Na, K, Ca, Mg)
  - 5.4.9 Total soil C and N
  - 5.4.10 Total phosphorus (P)
  - 5.4.11 POXC (permanganate oxidisable C)
  - 5.4.12 Phosphorus fractions: CEH Cambridge Citric acid extractable P, acetic acid extractable P, Olsen-P
  - 5.4.13 DNA, nitrogen genes
  - 5.4.14 Microbial diversity indices (16S rRNA and ITS; Illumina MiSeq)
  - 5.4.15 Soil water infiltration
  - 5.4.16 Water release curves; HYPRO-FIT modelling and related hydraulic parameters
- Data handling and quality control
  - QA/QC measures across labs; standard references, replicates, and cross-lab validation
  - Use of LIMS, Excel, and R for data processing; amplicon data processed with standard pipelines; MIAME-like QC for molecular data

## 5. Key datasets and measurements

- Agronomic outcomes
  - Yield (grass and wheat), biomass, biomass quality metrics (CP, ME, NDF, ADF, D value)
  - N content of crops, N offtake, nitrogen use efficiency (NUEc, NUEg)
- Greenhouse gas emissions
  - NH3 volatilisation (fluxes in appropriate units), N2O emissions (fluxes, cumulative)
- Soils and nutrients
  - N metrics (NH4+, NO3−, amino acids, mineralisable N), DOC/TDN
  - Microbial biomass C and N, DNA-based microbial community data (16S/ITS; OTUs and diversity indices)
  - Physical soil properties: texture, aggregate size distribution, SOM, moisture
  - Chemical soil properties: pH (multiple extractants), EC, base cations, total C and N, total P
  - P pools: Olsen-P, CEH citric acid extractable P, acetic acid extractable P
  - POXC as a soil quality indicator
- Physical processes
  - Soil infiltration rates and hydraulic conductivity; water release curves
- Modelling and analysis
  - N2O cumulative fluxes estimated via Bayesian MCMC approaches (JAGS), lognormal flux models, Delta and k parameters, and Nin fertilizer input scaling
  - NH3 modelling using dispersion models (FIDES) and inverse dispersion formulations
  - NUE and N content calculations standardized across sites and years

## 6. Outputs, access, and publications

- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Key publications arising from the datasets
  - Carswell et al. 2018: Assessing benefits and wider costs of different N fertilisers for grassland agriculture
  - Sánchez-Rodríguez et al. 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat
- Data handling emphasizes reproducibility, discoverability, and metadata-rich datasets via project portals

## 7. Appendices and supplementary material

- Appendix includes detailed experimental designs, fertiliser/digestate rates, and harvest dates (Tables A1–A3; Figures A1–A2)
- Additional methodological details for site layouts, pre-treatment information, and cross-site harmonisation