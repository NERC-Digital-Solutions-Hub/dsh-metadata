# Virtual Joint Centre for Improved Nitrogen Agronomy Supporting documentation for data

- The CINAg project aims to optimise farm practices and soil management to improve nitrogen use efficiency (NUE) and reduce environmental Nr losses, spanning China and the UK.
- The work is structured into four primary work packages (WP1–WP4):
  - WP1: Improved fundamental understanding of N cycling
  - WP2: Harnessing novel N technologies
  - WP3: Improved agronomic practices
  - WP4: Predictive capacity and knowledge exchange

## Project scope and data-relevant objectives

- Develop novel indicators of NUE and holistic soil-health metrics using real-time physical and chemical data to guide farm practices.
- Test and develop on-field experiments and farm platforms for sustainable intensification.
- Translate findings to Chinese farmers through established Science and Technology Backyard programmes.
- Datasets span across multiple UK farm platforms and UK-wide sites, enabling cross-site data integration and comparative analysis.

## Experimental platforms, sites, and study design

- Four primary UK farm platforms (2016–2017):
  - North Wyke (NW), Harpenden (HA), Henfaes Farm (HF), Easter Bush (EB)
  - Sites run fertiliser experiments with inorganic N sources; EB additionally hosted other experiments.
- 2018 UK-wide soil sampling across nine sites with at least two land uses per site (Scotland, Wales, England).
- Experimental formats:
  - Inorganic fertiliser experiments (grass trials) in 2016 across NW, HF, EB (grassland, three-cut silage system; total N applied ~240 kg N ha-1; treatments include urea, urea+inhibitor, AN, and controls).
  - Digestate experiment (winter wheat) in 2017 at NW and HF (digestate with/without nitrification inhibitor, acidified digestate, controls; target N from digestate ~190 kg N ha-1).
  - Additional grassland trials at EB and HA in 2017.
  - UK-wide sampling in 2018 to assess varying land uses and soil types (involving collaboration with UGRASS-related sites).
- Plot layouts varied by site and year (subplots for NH3 and N2O measurements, harvest/sub-sampling areas, and growth monitoring).

## Meteorological and site data

- NW and HF: daily rainfall, daily min/max temperatures; soil moisture sensors at 2.5 cm depth; WFPS calculations from soil bulk density and moisture readings.
- EB: soil temperature and WFPS measured; long-term data from permanent Easter Bush measurement station (air temp, soil temp, rainfall at 30-minute intervals).

## Core data types and indicators

- Plant yields and quality (grass and winter wheat):
  - Dry matter yields, crude protein, metabolisable energy, fibre metrics, digestibility, and related quality parameters.
- Nitrogen metrics:
  - N content in herbage, N offtake, nitrogen use efficiency (NUEc and NUEg).
  - For wheat, total N in harvested crop and NUE calculations.
- Greenhouse gases:
  - Ammonia (NH3) emissions and nitrous oxide (N2O) emissions (fluxes and cumulative fluxes).
  - Measurement methods include wind tunnels, static manual/automatic chambers, and dispersion/inverse models as appropriate by site.
- Soil nitrogen metrics (WP1 and WP2):
  - NH4+, NO3-, amino acids, peptides, mineralisable N.
  - DOC and TDN (with DON by difference).
- Soil microbial and genetic metrics:
  - Microbial biomass C and N (MBC/MBN).
  - DNA-based analyses: functional genes (nifH, amoA, nirK, nirS, nosZ, ureC) and 16S rRNA/ITS amplicon sequencing for bacteria, archaea, and fungi.
  - Diversity indices (Shannon, richness) and OTU analyses.
- Soil physical-chemical properties:
  - Aggregate size distribution, soil texture (sand, silt, clay), soil moisture, soil organic matter (LOI-based), pH, electrical conductivity (EC).
  - Base cations (Na, K, Ca, Mg) and total soil C and N.
  - Total P, extractable P pools (CEH Bangor: CEH Olsen-P; acetic acid extractable P for WP2), citric acid extractable P as a proxy for plant-available P.
  - POXC (permanganate oxidisable carbon) as a soil quality metric.
- Soil chemical pools and processes:
  - N metrics including mineral N pools and dissolvable N fractions; KCl-extractable Nr (NH4+/NO3-).
- Soil hydrology:
  - Soil water infiltration (infiltration rates) and soil water release curves (HYPRO/FIT modelling).
- Plant- and soil-associated spatial data:
  - Sample locations, plots, and land-use details across sites; biomass ceilings for aboveground measurements.

## Protocols and data processing (WP1 vs WP2)

- Sampling coordination:
  - Treatments sampled on the same day within each site; sampling dates adjusted for weather and crop phenology.
  - Harvests aligned with peak biomass per site management.
- Yields and quality:
  - Grass trials: multiple cuts per year with sub-sample analysis via NIR for quality metrics.
  - Wheat: grain and straw separated and weighed; grain moisture measured; 85% dry matter reporting.
- NUE calculations:
  - NUEc = (Nt - Nc) / Napplied × 100 for crop and NUEg for grain, with Nt as crop N offtake and Nc as control mean.
- GHG measurements:
  - NH3: wind-tunnel measurements with acid traps; cumulative NH3 calculated via area under the curve.
  - N2O: manual and/or automatic chambers; concentrations measured and fluxes calculated using standard flux equations; cumulative fluxes estimated with area under the curve and Bayesian approaches where applicable.
- Soil sampling methodology:
  - 0–15 cm topsoil cores and deeper cores as needed; WP1/wP2 sampling dates and depths specified for each site and year.
  - Soil extracts (KCl) for inorganic N, and multiple methods for NH4+/NO3-, amino acids, DON, DOC, MBC/MBN, etc.
- Lab analyses and QA/QC:
  - Colorimetric tests for NH4+/NO3-, malachite green for P, etc.
  - qPCR for nitrogen-cycle genes with triplicate amplifications, controls, and standards.
  - Amplicon sequencing (16S rRNA and ITS) with rarefaction and diversity analyses; negative controls included.
  - Two laboratory standards (BS1/BS3) and random replicates used for QA/QC across batches.
  - LIMS-based data handling and cross-lab data integration; data produced in Excel, with results later fed into project databases and analyses.
- Data processing and modeling:
  - N2O cumulative flux modeled with Bayesian MCMC approaches (JAGS) to estimate flux dynamics and emission factors.
  - Use of area-under-curve calculations, lognormal distributions for spatial and temporal flux patterns, and standard statistical tools in R (including lm, etc.).

## Data management, sharing, and outputs

- Project webpage provides access to project information and datasets.
- Key publications arising from the data:
  - Carswell et al. 2018: Assessing benefits and wider costs of different N fertilizers for grassland agriculture.
  - Sánchez-Rodríguez et al. 2018: Advanced processing of food waste-based digestate for mitigating nitrogen losses in winter wheat.
- Data assets cover a broad spectrum: agronomic yields, NUE metrics, NH3/N2O emissions, detailed soil N metrics, DOC/TDN, microbial gene abundances, OTUs/diversity, and soil physical properties.
- The datasets support cross-site comparisons, NUE optimization, and translation of findings to broader agricultural and environmental decision-making.

## Particular challenges and considerations for data leadership

- Data fragmentation and heterogeneity:
  - Data collected across multiple sites, years, and laboratories; reconciliation and harmonization are required for cross-site analyses.
- Granularity and data gaps:
  - Some sites have differing sampling densities and depths; certain measurements are site- or year-specific.
- Data quality and metadata:
  - Extensive QA/QC steps, calibration needs, and standardized protocols are essential to ensure consistency; metadata spans site, plot, treatment, sampling dates, and lab methods.
- Coordination and community engagement:
  - Cross-institutional collaboration (EH, Rothamsted, Bangor, CEH, etc.) necessitates robust data governance, version control, and discoverability.
- Practical translation:
  - Objectives include translating results to agronomic practice and to CAU/CAAS channels for farmer engagement, highlighting the need for practitioner-friendly data products and summaries.