# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- International project (China-UK) named CINAg aimed at optimizing farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce nitrogen losses to the environment.
- Objectives center on developing holistic soil health metrics, testing on-field practices, and translating knowledge to farmers via a proven programme.
- Structure organized into four Work Packages (WP1–WP4) focusing on understanding N cycling, novel N technologies, agronomic practices, and predictive capacity plus knowledge exchange.

## Project Aims and Work Packages
- WP1: Improve fundamental understanding of nitrogen cycling.
- WP2: Harness novel nitrogen technologies.
- WP3: Improve agronomic practices.
- WP4: Predictive capacity and knowledge exchange.

## Study design and sites
- Multi-platform, cross-UK and China/UK collaboration.
- Four UK farm platforms (2016–2017): 
  - North Wyke (NW) – Rothamsted Research
  - Harpenden (HA) – Rothamsted Research
  - Henfaes Farm (HF) – Bangor University
  - Easter Bush (EB) – Centre for Ecology & Hydrology, Edinburgh
- 2016: Inorganic fertilizer experiments on grassland.
- 2017: Digestate experiments on winter wheat; additional grassland trials at EB and HA.
- 2018: UK-wide soil sampling across nine sites with multiple land uses for biomass and soil assessments.
- 2018 sampling included two or more land-use types per site (e.g., arable, pasture, grazed grass, etc.).

## Data types and measurements
- Plant performance and nitrogen metrics:
  - Yields: dry matter, crude protein, metabolisable energy, fibre metrics, D-value, etc.
  - N content and N offtake; nitrogen use efficiency (NUEc for crop level; NUEg for grain).
- Soil and nutrient metrics (WP1 and WP2):
  - Inorganic N forms: NH4+, NO3−; amino acids and peptides; mineralisable N.
  - Soil organic/inorganic pools: DOC, TDN, DON; microbial biomass carbon and nitrogen (MBC/MBN).
  - Physical/chemical soil properties: aggregate size, texture, moisture, SOM (loss on ignition), pH, electrical conductivity (EC), base cations (Na, K, Ca, Mg).
  - Total soil carbon and nitrogen; total phosphorus; POXC.
  - Plant-available phosphorus: Olsen-P; citric acid extractable P; acetic acid extractable P.
  - DNA-based microbial analysis: nitrogen-cycling genes (nifH, amoA, nirK, nirS, nosZ, ureC) and microbial community diversity (16S rRNA, ITS) with OTUs and diversity indices.
  - Infiltration and soil water retention: water infiltration measurements and HYPRO-based water release curves (Mualem-Durner models).
- Greenhouse gas measurements:
  - Ammonia (NH3) emissions via wind tunnels and passive samplers; flux calculations from concentration differences and model inputs.
  - Nitrous oxide (N2O) emissions via static chambers (manual and automatic) and isotopic analysis; cumulative fluxes analyzed with Bayesian approaches and lognormal models.
- Sampling schedules and processing:
  - WP1: Topsoil sampling 0–15 cm; T0, T1, T2 timepoints for 2016; digestate-related sampling in 2017; 2018 topsoil sampling across land uses.
  - WP2: Intensive post-fertilization soil sampling (first weeks after N application), plus monthly sampling during the digestate trials.
- Biomass and yield sampling protocols vary by site and year, with harvest methods adapted to ensure peak biomass capture.

## Experimental protocols and design
- 2016 Inorganic fertilizer experiments (grass trials):
  - Treatments: Urea (U), Urea + inhibitor (IU), Ammonium-nitrate (AN), Control.
  - Uniform base fertilization with P, K, S; plots subdivided for NH3, N2O measurements and biomass harvest.
- 2017 Digestate experiments (winter wheat):
  - Treatments: Digestate only, Digestate + DMPP (nitrification inhibitor), Acidified digestate, Acidified digestate + DMPP, Control.
  - Digestate applied at ~190 kg N ha−1 with band-spread method; plots divided into harvest and sampling subplots.
- 2018 UK-wide sampling:
  - Sites with diverse land uses; biomass measurements across fields including exclosures where relevant (e.g., Silwood, Harpenden, Easter Bush, etc.).
  - Moss mesh deployments at Plynlimon to track moss growth and related dynamics.

## Data processing, analysis, and QA/QC
- Protocols differentiate WP1 and WP2 data collection and processing; synchronization of sampling across plots within sites.
- Yields and quality:
  - Grass yields converted to dry matter per hectare; N content derived from crude protein or direct analysis; NUE calculated as (Nt − Nc) / Napplied × 100 for crop and grain components.
- Ammonia and N2O calculations:
  - NH3: fluxes derived from wind-tunnel concentration differences, with area under the curve for cumulative emissions; EB site used inverse dispersion modeling (FIDES) for NH3 flux estimation.
  - N2O: manual and automatic chamber data; cumulative fluxes calculated via area-under-curve approaches; digestate trials normalized to % of N applied.
  - Bayesian approach (MCMC with Gibbs sampling in JAGS) used to estimate cumulative flux parameters (μlog, σlog, Δ, k); lognormal distributions underpin time-averaged flux modeling.
- Soil and biogeochemical analyses:
  - Standard colorimetric, spectrophotometric, and DNA-based methods across multiple labs; QA/QC includes laboratory standards, blanks, duplicates, and cross-lab validation.
  - Soil properties and nutrient pools reported on fresh weight and dry weight bases as appropriate; moisture corrections applied where needed.
- Microbial ecology:
  - qPCR quantification of nitrogen cycling genes; amplicon sequencing for bacterial (16S rRNA) and fungal (ITS) communities; diversity indices calculated using VegAN.
- Data management:
  - Data compiled in Microsoft Excel; LIMS (laboratory information management system) for final reporting; project webpage provides access to outputs and related publications.
- Appendices and references:
  - Detailed fertilizer and digestate treatment tables; site-specific harvest dates; methodological references for all assays; extensive bibliography for analytical methods.

## Data products, dissemination, and publications
- Datasets underpin publications such as:
  - Assessing the benefits and wider costs of different N fertilizers for grassland agriculture.
  - Spatial processing of digestate-derived nitrogen management for mitigating N losses in winter wheat.
- Project webpage and citations provided for data access and reproducibility.

## Endnotes and resources
- Public project portal: www.rothamsted.ac.uk/international/china/cinag
- Related datasets and methodological references spanning soil chemistry, microbial ecology, gas flux modeling, and plant physiology.