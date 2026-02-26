# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- Purpose: Documentation of the CINAg project data related to nitrogen management in UK agriculture, with aims to optimise farm practices and soil management to improve nitrogen use efficiency and reduce environmental losses.
- Key objectives:
  - Develop novel indicators of nitrogen use efficiency (NUE) and holistic soil health metrics.
  - Test and develop in-field experiments and farm platforms for sustainable intensification.
  - Translate findings to Chinese farmers via the Science and Technology Backyard programme.
- Structure (Work Packages):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Spatial scope and locations

- Four UK farm platforms (2016–2017) for fertiliser experiments:
  - North Wyke (NW, Devon), Harpenden (HA, Herefordshire), Henfaes Farm (HF, North Wales), Easter Bush (EB, near Edinburgh)
  - Each site has coordinates and field/plot layouts; Table 1 and Figure 1 summarize site names, coordinates, field names, and fertiliser types.
- Site characteristics:
  - NW: Stagni-vertic Cambisol (grass trial), Dystric Cambisol (winter wheat); textures clay loam to silty clay loam; MAT ~9.1°C; MAP ~1107 mm
  - HA: Chromic Luvisol/Alisol; clay loam to silty clay loam; MAT ~9.1°C; MAP ~686 mm
  - HF: Eutric Cambisol; sandy clay loam; MAT ~12.5°C (avg); MAP ~1060 mm
  - EB: Eutric Cambisol (imperfectly drained); clay loam; MAT/MAP not assessed
- Cross-UK soil and land-use sampling (2018):
  - Nine sites across Scotland, Wales, and England (Figure 2)
  - At least two land uses per site (table of land uses provided)

## Data collection and experimental design

- 2016 inorganic fertiliser experiments (grass trials):
  - Location: NW, HF, EB
  - Design: complete randomized blocks; four fertiliser treatments plus controls
  - Treatments: Urea (U), Urea + urease inhibitor (IU), Ammonium nitrate (AN), Control
  - Total N across plots: 240 kg N/ha
  - Sub-plot layout per site for NH3 measurements, soil sampling/N2O measurements, and biomass/Yield measurements
- 2017 digestate experiment (winter wheat):
  - Locations: NW and HF (with EB/HA additional grass trials)
  - Design: complete randomized blocks; five replicates per digestate treatment
  - Treatments: Digestate only, Digestate + nitrification inhibitor (DMPP), Acidified digestate, Acidified digestate + DMPP, Control
  - Target N from digestate: 190 kg N/ha (rates varied in field)
  - Sub-plot structure: harvest subplot and sampling subplot
- 2018 UK-wide sampling:
  - Sites selected to represent diverse land uses and soil types
  - Revisited sites from UGRASS project for soil sampling and aboveground biomass measurements
  - Involved grazing exclusion cages at actively grazed sites for biomass estimation

## Measurements and data types

- Yields and biomass
  - Grass: dry matter yields, acid detergent fibre, crude protein, metabolisable energy, NDF, D value
  - Wheat: grain and straw yields; moisture content; TGW
  - Methods: harvests per site with standard sub-sampling; NIR for quality metrics
- Nitrogen content and NUE
  - Grass N content (kg N/ha), N offtake (kg N/ha)
  - NUEc (crop NUE) and NUEg (grain NUE) calculated from N offtake and applied N
  - 2016 grass NUE derived from crude protein; 2017 wheat NUE from grain/straw N
- Greenhouse gases
  - Ammonia (NH3) emissions: wind-tunnel method (NW/HF); passive samplers; FNH3 calculations
  - Nitrous oxide (N2O) emissions: static chambers (manual and automatic at various sites); isotopic analysis at HF
  - Flux calculations: hourly/daily fluxes; cumulative fluxes via area under curve or Bayesian methods
- Soil sampling and metrics (WP1 and WP2)
  - Sampling depths: 0–15 cm (topsoil), 15–30 cm and below (as needed)
  - Nr (NH4+, NO3−), amino acids and peptides, mineralisable N
  - DOC and TDN; DON
  - Microbial biomass C and N (MBC/MBN)
  - Aggregate size distribution; soil texture (sand/silt/clay)
  - Soil moisture and soil organic matter (SOM) via LOI
  - Soil pH and electrical conductivity
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N; total P
  - POXC (permanganate oxidisable C)
  - Citric acid extractable P, acetic acid extractable P, Olsen-P
  - DNA and nitrogen cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC); qPCR data
  - Microbial diversity indices (Shannon, richness), OTUs and taxa abundances
  - Soil water infiltration (Mini Disk Infiltrometer) and water release curves (HYPRO/WP4)
- Data processing notes
  - Data compiled in Excel; QA/QC with standards, replicates, LIMS
  - N2O and NH3 fluxes integrated over time; Bayesian estimation used for N2O cumulative fluxes (JAGS/R)
  - Land-use and soil data linked to plot coordinates for GIS workflows

## Protocols, data processing, and quality assurance

- Sampling protocols differ for WP1 vs WP2; standardized site-level sampling days within sites
- Yields and N content calculations include standard conversion factors (e.g., crude protein to N content via 6.25)
- NH3: concentration measurements via acid traps and colorimetric analysis; fluxes derived from concentration changes and wind data
- N2O: manual and automatic chamber data processed with regression-based flux calculations; Bayesian/MCMC methods for cumulative flux estimation
- Soil analyses follow established methods (Mulvaney, Keeney, Murphy & Riley, etc.); QA/QC includes reference standards, random replicates, and cross-lab verification
- Molecular analyses: DNA extraction, qPCR for nitrogen cycling genes, amplicon sequencing for bacteria (16S) and fungi (ITS); rarefaction and diversity analyses conducted in R
- Data outputs include comprehensive metadata on sampling dates, plot layouts, treatment structures, and site characteristics to support GIS mapping and spatial analyses

## Data access, outputs, and references

- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Associated publications:
  - Carswell et al. 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Sánchez-Rodríguez et al. 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in a winter wheat crop
- Appendices and figures provide detailed fertiliser rates, harvest dates, and plot designs for reproducibility and spatial mapping

## Relevance for GIS Specialists

- Rich geospatial dataset framework:
  - Four main farm platforms with precise coordinates and historical treatment regimes
  - Nine UK-wide sampling sites with diverse land uses and soil types
  - Detailed plot-level layouts enabling spatial visualization of treatments (NH3/N2O measurements, biomass harvests, soil sampling points)
  - Meteorological and soil sensor data integration (weather stations, soil moisture probes)
- Multi-resolution data fusion:
  - Combines field experiment plots (mesoscale) with national-scale soil surveys (sites across the UK)
  - Harmonizes agronomic, biogeochemical, and microbial datasets for spatial analytics
- Potential GIS products:
  - Spatial maps of NUE, N losses (NH3/N2O), and soil health metrics across platforms and across the UK
  - Temporal GIS layers showing treatment effects, weather influences, and yield outcomes
  - Spatially explicit models of nitrogen cycling and transport linking field plots to broader landscape context