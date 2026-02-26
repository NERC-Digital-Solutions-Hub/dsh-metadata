# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Purpose and objectives
- The CINAg project aims to optimise farm practices and soil management to make better use of nitrogen sources and reduce environmental losses of nitrogen, mitigating associated impacts.
- Key objectives:
  - Develop novel indicators of nitrogen use efficiency (NUE) and combine them with real-time physical/chemical metrics to form holistic soil health and quality indicators to guide practice.
  - Use these indicators to test and develop on-field experiments and farm platforms for sustainable intensification.
  - Translate developments to Chinese farmers via the Science and Technology Backyard program developed by CAU and CAAS.
- Structure across four work packages (WP):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Project structure and sites
- Four UK farm platforms (2016–2017): North Wyke (NW, Devon), Harpenden (HA, Herefordshire), Henfaes Farm (HF, North Wales), Easter Bush (EB, near Edinburgh).
- 2018 UK-wide soil sampling across nine sites, with at least two land uses per site (varied across Scotland, Wales, and England).
- Site details include soil types, textures, mean annual temperature, and precipitation; cross-site collaboration encompassed the UGRASS network and other partners.
- 2018 sampling sites included a range of land uses such as pristine, cattle/grazed, arable rotations, park grass, broadbalk, and other agroecosystems.

## Experimental design and data types
- 2016 inorganic fertilizer experiments (grass trials) conducted across NW, HF, and EB; complete randomized blocks with four fertiliser treatments plus controls.
  - Treatments: Urea (U), Urea with urease inhibitor (IU), Ammonium-Nitrate (AN), Control.
  - Total N applied per site aimed at ~240 kg N ha-1, with P, K, S supplied per guidelines.
  - 2016 layouts included separate subplots for NH3 emission measurements, N2O emission measurements, and biomass/yield measurements.
- 2017 digestate experiment (winter wheat) at NW and HF; complete randomized blocks with five replicates per digestate treatment including digestate alone, digestate with nitrification inhibitor (DMPP), acidified digestate, acidified digestate with DMPP, and control.
  - Target digestate N application ~190 kg N ha-1 (rates varied by field constraints).
  - Plot sub-divisions for harvest and sampling; differential plot sizes by site.
  - EB/HA hosted additional grass trials in 2017.
- 2018 UK-wide sampling
  - Site selection encompassed diverse soil types and land uses; biomass measurements conducted across sites (grazing exclusion cages where applicable).
  - Sampling designed to capture broad-scale nitrogen dynamics across landscapes.

## Protocols and data processing
- Protocols are separated by WP1 and WP2 measurements, with synchronization of sampling days within a site.
- Yields and biomass (5.1)
  - Measured as dry matter yields (t ha-1), along with forage quality metrics (CP, ME, MAD, NDF, ADF, digestibility, etc.) using NIR analyses.
  - Grass trials: multiple harvests per year; winter wheat harvests conducted with plot-level yield separation (grain and straw) and moisture checks.
  - 2018 UK-wide: biomass estimates via grazing exclusion cages; some sites used external biomass estimates.
- N content, N offtake, NUE (5.2)
  - N content from crude protein (N content = CP × 0.160) to derive plant N; N offtake from grain/straw or harvested herbage; NUE calculated as (Nt - Nc) / Napplied × 100 for crops (and NUEg for grain).
- Greenhouse gas sampling: Ammonia and N2O (5.3)
  - Ammonia: wind tunnels with acid traps, multiple measurement positions, and C = concentration differences to compute fluxes; 2016 NW/HF and 2017 digestate methodologies varied slightly by site.
  - N2O: manual and automated static chambers; sampling schedules varied by site and treatment; fluxes derived by linear regression and cumulative fluxes calculated via area-under-curve approaches; 2018 EB used static chambers with GC analysis.
  - For digestate treatments, N losses expressed as percentage of total N applied (normalized for rate differences).
- Soil sampling and metrics (5.4)
  - WP1: soil cores 0–15 cm and deeper (15–30 cm, below) collected at multiple time points (e.g., pre-treatment T0, post-treatment T1, T2; additional 2018 sampling across land uses).
  - 5.4.1 Nr metrics: NH4+, NO3-, amino acids/peptides, mineralisable N via anaerobic incubation.
  - 5.4.2 DOC and TDN (DON inferred by difference).
  - 5.4.3 Microbial biomass C and N (MBC/MBN) via chloroform fumigation methods.
  - 5.4.4 Aggregate size distribution (laser diffraction; wet sieving).
  - 5.4.5 Soil texture (sand, silt, clay) via laser diffraction and standard corrections.
  - 5.4.6 Soil moisture and soil organic matter (SOM; LOI method).
  - 5.4.7 Soil pH and EC; WP1 and WP2 separate protocols.
  - 5.4.8 Base cations (Na, K, Ca, Mg) via ammonium acetate extraction and ICP-OES.
  - 5.4.9 Total C and N via combustion and chromatographic methods; QA/QC with standards.
  - 5.4.10 Total P via H2O2/H2SO4 digestion and colorimetric analysis.
  - 5.4.11 POXC (permanganate oxidisable carbon) via MnO4 oxidation and spectrophotometry.
  - 5.4.12 P pools: CEH Bangor (citric acid extractable P) and Olsen-P (Olsen extraction); acetic acid extractable P for WP2.
  - 5.4.13 DNA, nitrogen genes: qPCR targeting nifH, amoA (AOB/AOA), nirK/nirS, nosZ (I/II), ureC; sequencing for OTUs and microbial diversity.
  - 5.4.14 Microbial diversity indices: Shannon, richness; amplicon sequencing (16S rRNA for bacteria/archaea, ITS for fungi) with Illumina MiSeq; data processed via in-house pipelines and R (vegan) for diversity analyses.
  - 5.4.15 Soil water infiltration (Mini Disk Infiltrometer).
  - 5.4.16 Soil water release curves (HYPRO/Hyprop; Mualem-Durner and Peters-Durner models).
- Data management, QA, and dissemination
  - Data compiled in Excel files; advanced analyses conducted in R and JAGS for Bayesian inference (N2O flux modeling).
  - Quality control included standards, blanks, triplicates, and cross-lab QA.
  - Project webpage and linked publications provided for data access and dissemination.

## Outputs, dissemination, and references
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Notable publications from the data:
  - Carswell et al., 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Sánchez-Rodríguez et al., 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in a winter wheat crop
- Extensive methodological references supporting gas flux measurement, soil analyses, molecular methods, and statistical approaches are cited throughout.

## Appendices and supplementary materials
- Appendices include detailed fertiliser application rates, dates, and plot layouts (Tables A1–A3; Figures A1–A2).
- Pre-treatment information for the digestate experiments and site-specific plots.
- Supporting datasets and metadata accompany the published analyses.