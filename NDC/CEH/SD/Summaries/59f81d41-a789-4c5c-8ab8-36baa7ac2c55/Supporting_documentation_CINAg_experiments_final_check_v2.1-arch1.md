# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

## Overview
- Supporting documentation for the CINAg project, focused on improving nitrogen use and reducing environmental losses through integrated soil, crop, and management data.
- Combines field experiments, cross-UK site sampling, and advanced analyses (soil chemistry, microbial genetics, gas emissions, and soil physics) to develop indicators of nitrogen use efficiency (NUE) and holistic soil health metrics.

## Project aims and structure
- Aims to meet needs in China and the UK for optimized farm practices and soil management to improve NUE and reduce Nr losses.
- Objectives
  - 1) Develop novel NUE indicators and integrate real-time physical/chemical soil metrics.
  - 2) Use indicators to test and develop field experiments and farm platforms for sustainable intensification.
  - 3) Translate developments to Chinese farmers via the Science and Technology Backyard program.
- Work packages
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Study sites and platforms
- Four UK farm platforms (2016–2017) across the UK:
  - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
  - Coordinates and site details provided; soil types include Cambisols, Luvisols/Alisols, and Cambisols with varying drainage.
  - Abbreviations and field names used in Tables 1 and 2 (e.g., Beacon field, Skittle Alley, Highfield, Fosters Park, Grass Broadbalk, Horsepool, Engineers field, Upper Joiner Field).
- 2018 cross-UK soil sampling at nine sites with at least two land uses per site (Scotland, Wales, England):
  - Land-use combinations include pristine, cattle-grazed, arable rotations, permanent pasture, mown plots, etc. (Table 3).

## Meteorological and site data
- Weather data collection at NW and HF: daily rainfall and daily mean/min/max temperatures; soil moisture sensors at 2.5 cm depth for WFPS calculations.
- EB: soil temperature and WFPS measured with handheld probes; long-term data from Easter Bush measurement station (air temperature, soil temperature, rainfall at 30-min intervals).

## Experimental information and design
- Two multi-platform experiments (2016 and 2017):
  - 2016: Inorganic fertilizer trials on grassland at NW, HF, EB; complete randomized block design (EB had four control and four replicates per treatment).
    - Treatments: Urea (U), Urea with inhibitor (IU), Ammonium-nitrate (AN), Control.
    - Total N 240 kg ha-1; all plots received P, K, S per Defra guidelines.
    - Sub-plot layout for NH3, N2O, and biomass measurements; varying plot sizes by site.
  - 2017: Digestate trial on winter wheat at NW and HF; randomized block with five control plots and five replicates per digestate treatment.
    - Treatments: Digestate; Digestate + nitrification inhibitor (DMPP); Acidified digestate; Acidified digestate + DMPP; Control.
    - Target N application ~190 kg ha-1 as digestate; plots split into harvest and sampling subplots.
  - 2017 additional grass trials at EB and HA.
- UK-wide sampling (2018): soil sampling and aboveground biomass measurements across diverse land uses and soil types (nine sites).

## Protocols and data processing
- Distinct protocols for WP1 (soil, plant, and gas measurements before/during/after treatments) and WP2 (process-driven measurements during the post-application period).
- Harvests aligned with peak biomass, with weather-driven adjustments to sampling dates.

## Yields and biomass
- Grass yields: dry matter yields (t/ha), crude protein, metabolisable energy, fibre fractions, digestibility metrics, and related quality parameters.
- Methods varied by site (HF, NW, EB) but consistently involved sub-sampling, drying, and NIR analyses; harvest areas and timing adjusted per site.

## Nitrogen content, N offtake, and NUE
- N content and offtake calculated from crude protein data (N content derived via conversion factors; 6.25 standard factor for 2016 NW/HF grass data).
- NUE calculations:
  - NUEc = (Nt - Nc) / Napplied × 100 (whole crop)
  - NUEg = (Nt - Nc) / Napplied × 100 (grain-focused)
- Total N in harvested crops analyzed via Kjeldahl or equivalent methods; different sites employed consistent calculation formulas.

## Ammonia and nitrous oxide measurements
- Ammonia (NH3) emissions
  - NW and HF: wind-tunnel systems with acid traps; sampling frequency varied by treatment date; cumulative emissions calculated by area-under-curve methods.
  - EB: NH3 fluxes estimated using the FIDES inverse dispersion model with passive samplers at plot centers and plot edges.
- Nitrous oxide (N2O) emissions
  - NW: static manual chambers (n=4 per plot)
  - HF: combination of static manual and static automatic chambers with Isotopic N2O Analyser
  - EB: static chambers; samples analyzed by GC with ECD
  - Cumulative emissions calculated via area under the time-course or Bayesian approaches; temporal dynamics modeled with lognormal functions and MCMC (JAGS) for flux estimation.

## Soil sampling and metrics (WP1 and WP2)
- Soil sampling plans varied by project phase:
  - WP1: 0–15 cm topsoil cores; multiple sampling dates (T0, T1, T2) across 2016–2017; 0–30 cm and below for deeper analyses.
  - WP2: intensive soil sampling post-digestate and fertilizer applications; high-frequency sampling early post-application.
- Soil N metrics (NR metrics)
  - NH4+, NO3-, amino acids, peptides, mineralisable N
  - DOC and TDN; DON via subtraction
- Soil microbial and biogeochemical metrics
  - Microbial biomass C and N (MBC/MBN)
  - Aggregate size distribution; soil texture (sand, silt, clay)
  - Soil moisture, SOM (LOI), pH, EC
  - Base cations (Na, K, Ca, Mg)
  - Total soil C and N; Total P
  - POXC (permanganate oxidisable C)
  - Citric acid extractable P, acetic acid extractable P, Olsen-P
  - DNA: soil community DNA; qPCR targets for nitrogen-cycling genes (nifH, amoA AOA/AOB, nirK/nirS, nosZ I/II, ureC) and 16S rRNA and ITS for community analyses
  - Microbial diversity indices: Shannon, richness; OTUs and ITS analyses
- Soil physical properties
  - Soil infiltration (infiltration rate, hydraulic conductivity)
  - Soil water release curves and HYPRO-FIT modeling using Mualem-Durner/Bimodal models

## Data management and analyses
- Data compiled in Excel; standardization across sites and protocols.
- Analyses include near-infrared (NIR) for feed quality, colorimetric methods for inorganic N, gas flux calculations, and Bayesian/MCMC approaches for N2O flux modeling.
- Molecular data processing with Illumina MiSeq workflows, GreenGenes and UNITE databases, and R-based ecological analyses (vegan package).

## Outputs, datasets, and references
- Project webpage: www.rothamsted.ac.uk/international/china/cinag
- Publications arising from the datasets:
  - Carswell et al. 2018: Assessing the benefits and wider costs of different N fertilisers for grassland agriculture
  - Sánchez-Rodríguez et al. 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat
- Appendices provide detailed fertiliser rates, harvest dates, and pre-treatment information for digestate experiments.

## Additional notes
- The document emphasizes data traceability, cross-site comparability, and standardised metadata to enable discovery and reuse of datasets, aligning with the Analysts Answering Questions with Data archetype’s emphasis on data quality, standardisation, and reproducibility.