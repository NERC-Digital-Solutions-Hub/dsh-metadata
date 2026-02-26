# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- The CINAg project aims to optimise farm practices and soil management to make nitrogen use more effective and to reduce environmental nitrogen losses (Nr), thereby mitigating negative environmental impacts.
- Primary goals include developing novel indicators of nitrogen use efficiency (NUE) and holistic soil-health metrics, testing these in field experiments and farm platforms, and translating findings to Chinese farmers via the Science and Technology Backyard programme.

## Aims and structure

- Objectives:
  - Develop novel NUE indicators and combine them with real-time physical/chemical soil metrics to inform better farm practices and soil management.
  - Use these indicators to test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers to support poverty alleviation and community enrichment.
- Work packages (WP):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Experimental platforms and cross-UK sites

- Four UK farm platforms in 2016–2017:
  - North Wyke (NW) – Rothamsted-operated platform in Devon
  - Harpenden (HA) – Rothamsted Research, Herefordshire
  - Henfaes Farm (HF) – Bangor University, North Wales
  - Easter Bush (EB) – Centre for Ecology & Hydrology, Edinburgh
- 2018 UK-wide sampling at nine sites across Scotland, Wales, and England, with at least two land uses per site (e.g., arable, pasture, silage, park grass, etc.).
- Site characteristics captured: soil type, texture, mean annual temperature, and mean annual precipitation (as available).

## Experimental designs and treatments

- 2016 inorganic fertiliser experiments (grass trials):
  - Complete randomized block design at NW, HF, and EB.
  - Treatments: 
    - Urea (U)
    - Urea with urease inhibitor (IU)
    - Ammonium-nitrate (AN)
    - Control
  - Total N applied per site: 240 kg N ha−1
  - Subplot allocations per site for NH3 measurements, N2O measurements, and biomass/yield analyses
- 2017 digestate experiments (winter wheat):
  - Complete randomized block design at NW and HF with five replicates per digestate treatment plus controls
  - Treatments:
    - Digestate only
    - Digestate + nitrification inhibitor (DMPP)
    - Acidified digestate
    - Acidified digestate + nitrification inhibitor
    - Control
  - Target N from digestate: 190 kg N ha−1 (rates varied in practice)
  - Plot layout included separate harvest and sampling subplots
- 2017 additional grassland trials at EB and HA
- 2018 UK-wide sampling:
  - Sites chosen with diverse land uses; repeated sampling for aboveground biomass and soil/vegetation metrics

## Measurements and protocols

- Yields and biomass (WP1 & WP2)
  - Dry matter yields (tonnes per ha) and quality metrics (crude protein, metabolisable energy, NDF, ADF, etc.)
  - Harvest methods varied by site; multiple cuts for grass trials; single harvest for winter wheat trials
- N content, N offtake and NUE (WP1)
  - Grass N content converted from crude protein where needed
  - Offtake and NUEc (total crop N offtake minus control, divided by N applied) and NUEg (grain N offtake)
- Greenhouse gas sampling: Ammonia (NH3) and nitrous oxide (N2O)
  - NH3: wind tunnels and acid traps; cumulative NH3 fluxes calculated per plot
  - N2O: manual and/or automatic chambers; gas chromatography and isotopic analyses (where applicable)
  - For EB, NH3 fluxes estimated with a dispersion model (FIDES)
  - Bayesian methods used to estimate cumulative fluxes (lognormal distributions; MCMC with JAGS)
- Soil sampling and metrics (WP1 and WP2)
  - NH4+, NO3−; amino acids and peptides; mineralisable N
  - DOC/TDN; DON calculations
  - Soil microbial biomass C and N (MBC/MBN)
  - Aggregate size distribution; soil texture (sand, silt, clay)
  - Soil moisture and soil organic matter (SOM) by LOI
  - pH and electrical conductivity (EC)
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N; total P
  - POXC (permanganate oxidisable carbon)
  - Phosphorus fractions: citric acid extractable P, acetic acid extractable P, Olsen-P
- DNA and nitrogen-cycling genes (5.4.13–5.4.14)
  - DNA extraction from soil; qPCR targeting nifH, amoA (AOB/AOA), nirK, nirS, nosZ (clade I & II), ureC
  - 16S rRNA and ITS amplicon sequencing for bacterial and fungal diversity; diversity indices (Shannon, richness)
- Plant, soil, and environmental data integration
  - Aboveground biomass measurements and periodic soil sampling aligned across sites
  - Data quality controls included reference standards, blanks, and QA processes
- Additional measurements
  - Soil water infiltration (Mini Disk Infiltrometer)
  - Soil water release curves and hydraulic parameters (HYPRO-FIT, Mualem-Durner model)
  - Meteorological data collection at multiple sites (rainfall, temperature, soil temperature, soil moisture)

## Data processing, analysis, and methodologies

- Data processing approaches:
  - Yields and biomass converted to standard units; factors applied for protein and N calculations where needed
  - NUE calculations use standard equation: NUE = (Nt − Nc) / Napplied × 100
  - N2O and NH3 emissions quantified per plot and period; area-under-curve or Bayesian models used for cumulative fluxes
  - Ion concentrations (NH4+, NO3−) and other soil N metrics calculated from standard colorimetric methods
  - DNA/qPCR results converted to gene copy numbers per gram of dry soil; amplicon sequences processed with established pipelines
- Statistical and modeling approaches:
  - Bayesian inference for cumulative N2O and related fluxes (MCMC with JAGS)
  - Lognormal distributions used to describe flux data and spatial variability
  - Cumulative flux corrections account for control plots and different N inputs
- Data management and reproducibility:
  - Protocols and dates maintained; datasets organized by WP and site
  - Metadata and data provenance tracked; datasets intended to be discoverable via portals

## Datasets, portals, and publications

- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Key publications derived from CINAg data:
  - Carswell et al., 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Sánchez-Rodríguez et al., 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat
- Data scope includes site-level and UK-wide soil, crop, and gas emission datasets, with detailed protocols and QA steps described in the supporting documentation

## Appendices and supporting materials

- Appendix includes:
  - 8.1 Inorganic fertiliser experiment (2016) – detailed application rates and harvests
  - 8.2 Digestate experiment (2017) – plot layouts and treatments
  - Pre-treatment information for digestate experiments and plotting schemes
- Figures illustrating farm platforms, site locations, and experimental designs
- Tables with site-specific soil types, textures, MAT, and MAP where available

## Practical relevance for data analysts

- Provides a comprehensive, cross-site dataset encompassing agronomy, soil health, nutrient cycling, and greenhouse gas emissions with standardized metrics and protocols.
- Enables analysis of NUE under different N sources (inorganic vs digestate), inhibitors, and acidification strategies, across multiple UK platforms.
- Supports development and validation of predictive indicators for soil health and N-use efficiency, with robust QA, metadata, and data archiving practices.
- Facilitates cross-disciplinary analyses linking soil chemistry, microbial ecology, plant productivity, and environmental emissions.