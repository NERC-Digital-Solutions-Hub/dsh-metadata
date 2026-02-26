# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Aims to use data to demonstrate environmental condition and policy performance over time, focusing on nitrogen (Nr) management to reduce environmental losses.
- CINAg project goals emphasize developing NUE indicators and holistic soil-health metrics, testing on-field farm platforms, and translating findings to farmers through established programs.
- Project structure organized into four work packages (WP1–WP4) addressing fundamental N cycling, novel N technologies, agronomic practices, and predictive capacity plus knowledge exchange.

## Project overview and structure

- Objective 1: Develop novel indicators of N use efficiency (NUE) combined with real-time physical/chemical soil metrics to inform farming practices and soil management for better agronomic NUE and sustainable crop production.
- Objective 2: Use indicators and new knowledge to test on-field experiments and farm platforms for sustainable intensification.
- Objective 3: Translate developments to Chinese farmers via the Science and Technology Backyard program (CAU/CAAS).
- WP1: Improved fundamental understanding of N cycling
- WP2: Harnessing novel N technologies
- WP3: Improved agronomic practices
- WP4: Predictive capacity and knowledge exchange

## Locations and platforms

- Four UK farm platforms (2016–2017): North Wyke (NW), Harpenden (HA), Henfaes (HF), Easter Bush (EB).
  - NW and HA operated by Rothamsted Research; HF by Bangor University; EB by CEH.
  - Coordinates and site characteristics summarized in tables; soils include Stagni-vertic Cambisol, freely draining Luvisols, Cambisols, etc.
- 2018 UK-wide sampling: nine sites across Scotland, Wales, and England with at least two land uses per site (site-to-site variability in land use and soil type).
- Figures and tables depict locations, site soils, climates (MAT/MAP), and land-use diversity.

## Experimental design and treatments

- 2016 inorganic fertiliser experiments (grass trials):
  - Locations: NW, HF, EB
  - Complete randomized block design with four fertiliser treatments and four replicates per site:
    - 1) Urea (N ~46%)
    - 2) Urea with urease inhibitor (IU)
    - 3) Ammonium-nitrate (AN, NH4+/NO3−)
    - 4) Control
  - Total N application around 240 kg N ha−1; plots also received P, K, S as per guidelines.
  - Sub-plot structure varied by site, enabling NH3 emission measurements, N2O emission measurements, and biomass/yield assessments.
- 2017 digestate experiment (winter wheat):
  - Locations: NW and HF
  - Complete randomized block design with five replicates and five treatments:
    - 1) Digestate only
    - 2) Digestate + nitrification inhibitor (DMPP)
    - 3) Acidified digestate
    - 4) Acidified digestate + DMPP
    - 5) Control
  - Target N-rate: 190 kg N ha−1 as digestate (actual rates varied); digestate band-spread in crop rows.
  - Harvest and sampling subplots established for WP1 and WP2 analyses.
- 2018 UK-wide sampling:
  - Re-visitation of sites from UGRASS project; measurement of aboveground biomass and soil properties across diverse land uses.

## Data collected and indicators

- Yields and biomass
  - Grass yields (ton/ha dry matter), quality metrics (CP, ME, ADF, NDF, D value, etc.)
  - Winter wheat yields (grain and straw), thousand-grain weight, moisture; harvest area-based estimates
- Nitrogen content and NUE
  - Herbage N content, N offtake; NUEc (crop total N uptake) and NUEg (grain N uptake)
  - Calculations based on yield data and N content, with control corrections
- Greenhouse gases
  - Ammonia (NH3) emissions (kg NH3-N ha−1 day−1) via wind tunnels or dispersion models
  - N2O fluxes (μg N2O-N m−2 h−1) via static chambers (manual and automated)
  - Cumulative N2O emissions over fertilisation periods using area-under-curve methods and Bayesian/MCMC approaches
- Soil nitrogen metrics (WP1 and WP2)
  - NH4+ and NO3−, amino acids, peptides, mineralisable N
  - DOC and TDN (and DON by difference)
- Soil biology and microbial metrics
  - Soil microbial biomass C (MBC) and N (MBN)
  - DNA, nitrogen cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC) and microbial diversity indices
  - OTUs and diversity (Shannon, richness) from amplicon sequencing (16S rRNA, ITS)
- Soil physical and chemical properties
  - Aggregate size distribution; soil texture (sand, silt, clay)
  - Soil moisture and soil organic matter (SOM)
  - pH and electrical conductivity (EC)
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N; total P
  - POXC (permanganate oxidisable carbon)
  - Plant-available P pools: citric acid-extractable P, acetic acid extractable P, Olsen-P
- Soil nutrient pools and processes
  - Nr extraction (NH4+, NO3−) and mineral N metrics
  - Soil infiltration and soil water release curves (hydraulic parameters)
- Infiltration and hydrology
  - Soil water infiltration rates and hydraulic conductivity
  - HYPRO-FIT modelling to model water retention curves and conductivity

## Protocols and data processing

- Distinct sampling protocols for WP1 (fundamental N cycling) and WP2 (novel N technologies); sampling days aligned to site conditions and harvests.
- Yields and biomass
  - Harvested with field equipment; sub-samples analysed for quality (NIR) and composition
- Nitrogen content and NUE calculations
  - Grass N content derived from crude protein where needed
  - NUE calculations reference control plots and total fertilizer applied
- Greenhouse gas measurements
  - NH3: wind tunnels and acid traps; concentration measurements; cumulative NH3 via area under the curve
  - N2O: manual and automatic chambers; gas chromatography and isotopic analyses; Bayesian upscaling and MCMC (JAGS) for cumulative flux
  - Models account for background concentrations and source strengths; time- versus space-structured uncertainties
- Soil sampling (WP1 and WP2)
  - Topsoil cores (0–15 cm) and deeper layers; field sampling dates and depths detailed
  - Chemical extraction protocols for inorganic N (NH4+, NO3−), mineralisable N, amino acids, DON
  - DOC/TDN measurements from K2SO4 extracts; POXC via KMnO4 method
  - P pools via CEH and Olsen methods; rapid colorimetric assays with QA/QC using standards
- Soil physical and chemical properties
  - Texture by laser diffraction; aggregate size distribution by sieving and laser methods
  - SOM by LOI; moisture content by oven-drying
  - pH and EC by standard soil-water and soil-CaCl2 suspensions
  - Base cations by ammonium acetate extraction and ICP-OES
  - Total C and N by elemental analysis (CEH, Bangor, Rothamsted)
- DNA and microbial analyses
  - DNA extraction from soils; qPCR for nitrogen-cycling genes; amplicon sequencing for bacterial/archaeal and fungal communities
  - Diversity analyses in R using vegan package; standard curves and controls included
- Infiltration and water retention
  - Infiltration measured with Mini Disk Infiltrometer; water retention curves via HYPRO-FIT and related methods
- Data management and QA/QC
  - Data compiled in Excel; Lab standards (BS1/BS3), blanks, and replicates included
  - Instrument calibration checks and cross-site QA/QC procedures
  - Analyses conducted with R (various versions) and JAGS for Bayesian inference

## Data access, outputs, and publications

- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Datasets underpinning several publications:
  - Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Advanced processing of food waste-based digestate for mitigating nitrogen losses in a winter wheat crop
- The documentation supports cross-site data synthesis, enabling assessment of environmental health and policy-relevant performance of nitrogen management.

## Key challenges and opportunities for analysts

- Increasing the value of datasets by integrating monitoring data with other relevant environmental datasets (farms, soils, climate, biodiversity).
- Enhancing data accessibility to enable broader use by researchers, policymakers, and practitioners beyond the project partners.