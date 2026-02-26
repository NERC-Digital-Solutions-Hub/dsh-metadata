# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview and aims
- multi-site CINAg project to optimise farm nitrogen practices and soil management, reducing environmental Nr losses and improving agronomic NUE.
- Objectives: develop novel NUE indicators and holistic soil-health metrics; test on-field experiments and farm platforms; translate findings to Chinese farmers via Science and Technology Backyard.
- Structure: four work packages (WP1–WP4) covering N cycling fundamentals, novel N technologies, improved agronomic practices, and predictive capacity/knowledge exchange.

## Data sources and platforms
- four farm platforms across the UK (North Wyke, Harpenden, Henfaes, Easter Bush) for inorganic fertiliser and digestate experiments (2016–2017); additional UK-wide sampling in 2018.
- cross-UK site network (nine sites) for soil and aboveground biomass measurements (2018), with multiple land uses per site.
- cross-project data sharing and deployment through project webpages and associated publications.

## Experimental design and locations
- 2016: inorganic fertiliser grass trials conducted at NW, HF, EB (three-site randomized block design with four fertiliser treatments plus controls; subplots for NH3, N2O, and biomass).
- 2017: digestate experiment on winter wheat at NW and HF (randomized block with five replicates per digestate treatment; subplots for harvest and sampling).
- 2017: additional grassland trials at EB and HA.
- 2018: UK-wide soil sampling across nine sites with at least two land uses per site.

## Meteorological and site data
- NW and HF: daily rainfall and temperatures; soil moisture sensors for water-filled pore space (WFPS) at 2.5 cm depth.
- EB: soil temperature and WFPS measured; long-term measurements from Easter Bush station (air temp, soil temp, rainfall at 30 min intervals).
- Site-specific soil types, textures, and mean annual temperature/rainfall summarized (Tables 1–2, Figure 1).

## Data types and measurements

### 1) Yields and biomass
- Grass trials: dry matter yields, crude protein, metabolisable energy, fibres, digestibility metrics, etc.
- Wheat trials: grain and straw yields, grain moisture, thousand-grain weight; end-of-season biomass where applicable.
- Methods: multiple cuts/harvests per year; subsampling for quality analyses; NIR analysis for quality metrics.

### 2) Nitrogen content, N uptake and NUE
- Grass N content (converted from crude protein, 6.25 factor) and N offtake per hectare.
- Wheat N content in grain and straw; NUE at crop (NUEc) and grain (NUEg) levels calculated from N uptake and N applied.
- Data processing includes normalization to plots and harvest areas.

### 3) Greenhouse gases: NH3 and N2O
- NH3: emissions measured with wind tunnels and passive samplers; cumulative NH3 flux calculated per plot; multi-method approach across sites (inorganic fertiliser and digestate experiments; EB site uses dispersion modeling for fluxes).
- N2O: fluxes measured with static chambers (manual and automatic) across sites; flux calculations per chamber and plot; cumulative fluxes modeled using Bayesian approaches (lognormal distributions; MCMC in JAGS).
- Outputs include cumulative fluxes and treatment comparisons normalized to N applied.

### 4) Soil sampling and soil metrics (WP1 and WP2)
- Sampling depths: primarily 0–15 cm topsoil; additional deeper cores as needed.
- Nr metrics: NH4+, NO3-, amino acids, peptides, mineralisable N; DON and DOC/TDN; soil microbial biomass C and N (MBC/MBN); aggregate size distribution; soil texture; soil moisture and SOM; pH and EC; base cations (Na, K, Ca, Mg); total soil C and N; total P.
- P fractions: permanganate oxidisable C (POXC); citric acid extractable P, acetic acid extractable P, Olsen-P.
- DNA and microbial function: DNA extractions; qPCR for nitrogen-cycle genes (nifH, amoA AOB/AOA, nirK/nirS, nosZ I/II, ureC); OTUs and microbial diversity indices (16S rRNA, ITS); amplicon sequencing (MiSeq) with taxonomic assignments (GreenGenes, UNITE); diversity metrics (Shannon, richness).
- Soil process measurements: soil water infiltration (mini-disk infiltrometer); soil water release curves (HYPRO/HYPRO-FIT) and Mualem–Durner modeling.
- 5.4.13–5.4.16 include detailed molecular, biochemical, and physical soil assessments with QA/QC procedures.

## Protocols, data processing and QA
- Distinct protocols for WP1 vs WP2, with all plots sampled on the same day within a site; sampling cadence aligned to fertiliser events and growth stages.
- Data processing: unit conversions, harvest-area adjustments, and calculation formulas (e.g., NUE equations, NH3/N2O flux calculations, digestate N recoveries).
- QA/QC: use of laboratory standards, replicate analyses, and cross-site QA; traceability via LIMS, instrument calibration, and reference samples.
- Analytical labs involved include Rothamsted Research, Bangor University, CEH Bangor, CEH Lancaster, CEH Wallingford, and others.

## Data products, outputs and dissemination
- Primary outputs: datasets enabling self-service data exploration (dashboards, pivotable summaries), and comprehensive reports by WP.
- Outputs inform on N-use efficiency indicators, soil health metrics, and GHG budgets under different nitrogen sources.
- Publications and project outputs for broader dissemination:
  - Carswell et al. 2018: benefits and costs of different N fertilisers for grassland.
  - Sánchez-Rodríguez et al. 2018: processing of digestate for N-loss mitigation in winter wheat.
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Outputs intended for farmer outreach via Science and Technology Backyard programs and cross-UK knowledge exchange.

## Key challenges and considerations for data support
- Heterogeneous data formats across sites and years; need for harmonization and metadata standardization.
- Patchy data due to weather, logistics, and field conditions; robust QA and provenance tracking essential.
- Cross-system data integration (soil, plant, gas fluxes, molecular data, meteorology) for holistic NUE and soil-health indicators.
- Clear data sharing and access strategy to promote reuse, re-analysis, and adoption by end users.

## Endnotes and references
- Supporting documentation outlines experimental designs, protocols, and data processing steps in detail (Appendices with fertiliser rates, layouts, and site-specific data).
- Key references cited for methods and modeling approaches (e.g., N2O flux modeling, NH3 dispersion, soil analyses, and molecular methods) and links to related datasets and publications.