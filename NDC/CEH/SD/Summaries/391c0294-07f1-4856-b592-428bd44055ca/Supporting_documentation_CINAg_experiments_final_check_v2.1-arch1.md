# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- International CINAg project (China-UK collaboration) to optimise farm practices and soil management for improved nitrogen use efficiency (NUE) and reduced environmental Nr losses.
- Aims to develop holistic soil-health metrics and real-time indicators, test in field/farm platforms, and translate findings to Chinese farmers through Science and Technology Backyard programmes.

## Aims and objectives
- Develop novel, robust NUE indicators combined with real-time physical/chemical soil metrics to guide farm practices and soil management.
- Use indicators to test and develop on-field experiments and farm platforms for sustainable intensification.
- Translate developments to Chinese farmers to support rural livelihoods and community benefits.
- Structure into four work packages:
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Work packages at a glance
- WP1: Deeper understanding of nitrogen cycling processes
- WP2: Deployment and assessment of novel nitrogen technologies
- WP3: Evaluation and improvement of agronomic practices
- WP4: Predictive modelling, capacity building, and knowledge exchange

## Experimental platforms and cross-UK sites (3.1–3.2)
- Four UK farm platforms (2016–2017): 
  - North Wyke (NW, Rothamsted-operated plots), Harpenden (HA, Rothamsted), Henfaes Farm (HF, Bangor University), Easter Bush (EB, CEH)
- 2016 inorganic fertiliser experiments (grass trials) conducted at NW, HF, EB
- 2017 digestate experiment (winter wheat) conducted at NW and HF; additional grass trials at EB and HA
- 2018 UK-wide sampling across nine sites (two+ land uses per site; Scotland, Wales, England)
  - Land uses sampled include pristine, cattle-grazed, arable rotations, park grass, mixed systems, dunes, etc. (Table 3 details per site)
- Site information highlights:
  - NW: Stagni-vertic Cambisol and Dystric Cambisol soils; clay loam/silty textures; MAT ~6.9–13.8°C; MAP ~1107 mm
  - HA: Chromic Luvisol/Alisol; clay loam to silty clay loam; MAT ~9.1°C; MAP ~686 mm
  - HF: Eutric Cambisol; sandy clay loam; MAT ~9.5°C; MAP ~1060 mm
  - EB: Eutric Cambisol (imperfectly drained); clay loam; MAT/precipitation not assessed

## Meteorological data at the four farm platforms
- NW and HF: daily rainfall, mean/min/max temperatures; soil moisture (10 cm depth) via SDI-12 sensors; soil bulk density for pore-space calculations
- EB: soil temperature and water-filled pore space via handheld probes; long-term data from Easter Bush measurement station (air temp, soil temp, rainfall at 30-min intervals)

## Experimental information
- Two multi-platform experiments (2016 and 2017)
  - 2016 Inorganic fertiliser trials (grass):
    - Sites NW, HF, EB; 3-cut silage system; total N 240 kg N/ha
    - Randomised block design (NW/HF); EB with 4 control plots and 4 replicates per fertiliser treatment
    - Treatments: 
      - Urea (U, ~46% N)
      - Urea + inhibitor (IU)
      - Ammonium-Nitrate (AN, ~36% N)
      - Control
  - 2017 Digestate experiment (winter wheat):
    - Complete randomised block design at NW and HF; five control plots and five replicates per digestate treatment
    - Treatments: digestate only; digestate + nitrification inhibitor (DMPP); acidified digestate; acidified digestate + DMPP; control
    - Target N application: 190 kg N ha^-1 as digestate (rates varied by plot)
- 2018 UK-wide sampling
  - Sites with varied land uses and soils; some re-visited from UGRASS project for soil sampling and aboveground biomass measurements

## Protocols and data processing
- Distinct sampling protocols for WP1 and WP2; all plots sampled the same day within a site
- Crops harvested after full season as advised by farm managers

### 5.1 Yields and biomass production
- Measurements across sites NW/HF/EB; 2016 grass trials used multi-cut yields
- Quality metrics: crude protein, metabolisable energy, fibre metrics, digestibility, moisture
- Harvest methods varied by site (central strips, subplots, hand-harvest, or small-plot combine)
- Units: tonnes ha^-1 DM yield, CP, ME, MAD, D-value, N content indicators, TGW, etc.

### 5.2 Wheat N content, N offtake and NUE
- N content derived from crude protein or direct total N analyses; N offtake from grain and straw
- NUE calculated as (Nt - Nc) / Napplied × 100 for total crop; NUEg for grain
- EB used Kjedahl-based total N; methodology consistent with above equations

### 5.3 Sampling of greenhouse gases: NH3 and N2O
- NH3: wind tunnels at NW/HF; passive samplers at multiple heights; concentration-derived flux calculations
- N2O: manual and/or automatic chambers depending on site; sampling frequency high around fertiliser events; cumulative emissions via area-under-curve
- Digestate 2017: N-loss expressed as percent of N applied relative to controls
- EB: NH3 fluxes estimated using FIDES inverse dispersion model
- Bayesian framework for cumulative fluxes at EB and other sites; lognormal distribution assumptions and MCMC (JAGS)

### 5.4 Soil sampling and analyses
- WP1 and WP2 soil sampling protocols; 0–15 cm topsoil cores, additional deeper cores as needed
- WP1: 2016 and 2017 T0/T1/T2 sampling schedules; 2018 multiple land uses with 0–15 cm sampling
- 2016/2017 soil analyses include:
  - Nr: NH4+/NO3-, amino acids, peptides, mineralisable N
  - DOC/TDN; DON as TDN minus inorganic N
  - QA/QC with standards and replication
- 5.4.2 DOC and TDN measured in K2SO4 extracts via analyzers
- 5.4.3 MBC/MBN via chloroform fumigation method
- 5.4.4 Aggregate size distribution via sieve and laser diffraction
- 5.4.5 Soil texture by laser diffraction; validation with standard soils
- 5.4.6 Soil moisture and SOM by LOI and moisture content methods
- 5.4.7 Soil pH and EC (WP1 and WP2) using standard extraction methods
- 5.4.8 Base cations (Na, K, Ca, Mg) by ammonium acetate extraction and ICP-OES
- 5.4.9 Total C and N by elemental analysis (WP1, WP2) with QA/QC
- 5.4.10 Total P by H2O2/H2SO4 digestion and colorimetric analysis
- 5.4.11 POXC by permanganate oxidation with colorimetric readout
- 5.4.12 P fractions:
  - CEH: citric acid extractable P (Ca-bound/plant-available pool) via Malachite Green
  - Olsen-P via bicarbonate extraction and colorimetric measurement
  - Acetic acid extractable P (proxy for plant-available P in WP2)
- 5.4.13 DNA, nitrogen genes
  - Soil DNA extraction; qPCR for nifH, amoA (AOB/AOA), nirK/nirS, nosZ, ureC
  - 10 µL reactions in a 384-well format; triplicate analyses; standard curves and controls
- 5.4.14 Microbial diversity indices
  - 16S rRNA and ITS amplicon sequencing (MiSeq); analysis pipelines for bacteria and fungi
  - Diversity metrics: Shannon, Richness; OTUs and actual sequence variants; rarefaction
- 5.4.15 Soil water infiltration
  - Mini Disk Infiltrometer; multiple tensions; HYPROP macro for hydraulic parameters
- 5.4.16 Soil water release curves
  - HYPROP and WP4 methods; bimodal retention curves (Mualem-Durner model) and Peters–Durner model for conductivity

## Data management, QA/QC, and dissemination
- Rigorous QA/QC across laboratories and laboratories’ standards
- Data compiled in Excel; metadata and datasets prepared for discovery via portals
- Data sources linked to project outputs; site and protocol details documented in appendices
- Publications and project web presence:
  - Project webpage: www.rothamsted.ac.uk/international/china/cinag
  - Related publications (2018): several on N fertilisers, digestate processing, and soil-nitrogen dynamics
- Data and methods designed to be discoverable and reusable, with metadata and cross-dataset integration in mind

## Notable outputs and references
- Publications:
  - Assessing the benefits and wider costs of different N fertilisers for grassland agriculture (Archives of Agronomy and Soil Science, 2018)
  - Advanced processing of food waste-based digestate for mitigating nitrogen losses in wheat (Frontiers in Sustainable Food Systems, 2018)
- References span analytical methods for soil N metrics, gas measurements, molecular analyses, and statistical approaches (e.g., MCMC with JAGS, lognormal flux modeling)