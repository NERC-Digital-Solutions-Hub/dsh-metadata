# Environmental conditions, ozone concentrations, biomass and leaf level functional traits data for 10 tropical tree species grown across a range in ozone concentrations within nine Open Top Chambers in Cairns, Australia.

## Overview
- Dataset from July 2020 to November 2022 measuring ozone (O3) concentrations, environmental conditions, final biomass, and leaf-level functional traits for 10 tropical tree species.
- Part of the TropOz project (NE/R001812/1) examining ozone impacts on tropical vegetation and forest productivity.
- Complementary data set available: TropOz data collaboration link provided.

## Experimental Facility and Plant Material
- Conducted at the TropOz research facility (UoE/JCU) in far-north Queensland, Australia.
- Nine independently controlled Open Top Chambers (OTCs) with a gradient of nine O3 exposures (8:00–17:00 fumigation).
- Chamber mean O3 concentrations ranged from 25 to 112 ppb during exposure.
- Environmental monitoring included continuous O3 analysis and high-resolution meteorological data (air temperature, relative humidity, shortwave radiation, PAR).
- Ten tropical tree species across nine families were studied; includes detailed species list and family associations.
- Seedlings sourced locally; grown in pots with garden mix + scoria; plants acclimated to full sun before transfer to OTCs.
- Treatments lasted 61–191 days (average ~150 days); plants irrigated daily and fertilized as needed.
- Harvested plants were separated into leaves, stems, and roots for dry biomass and biomass partitioning analyses.

## Data Collected and Measurements
- O3 concentrations in each chamber, with high-resolution time series.
- Meteorological variables (temperature, relative humidity, PAR) used to derive inputs for DO3SE modelling.
- Plant biomass data: final dry weights for leaves, petioles, stems, roots; total above-ground biomass (AGB) and total biomass; leaf area (LA_Av) and leaf mass per area (LMA, including lamina LMA).
- Leaf biochemical traits: 
  - Total carbon (TC) and nitrogen (TN) and stable isotopes (δ13C, δ15N).
  - Total Antioxidant Capacity (TAC) via FRAP assay.
  - Total Phenolic Content (TPC) via Folin-Ciocalteau assay.
- Leaf sampling protocol: multiple leaves per plant; lamina tissue extraction for biochemical analyses; samples stored and processed under specified conditions.

## Data Structure and Files
- DO3SE model parameters (DOS3E_inputs.csv): 15 columns including species code, m, g0, Vcmax, Jmax, gmax_O3, fmin, Tmin, etc., for species-specific DO3SE parameterization.
- DO3SE inputs data files: ten files named speciescode_merged_data.csv (e.g., Ba_merged_data.csv) containing 17 columns per file with time-resolved environmental and chamber O3 data, including Day_of_year, Hour_of_day, Temperature, VPD, PAR, Pa, Wind, ppt, and Cham_1 to Cham_9 O3 concentrations.
- Experimental_Biomass.csv: 19 columns including Code, Plant_ID, Cham_ID, Leaves_dw, Petiole_dw, Stems_dw, Roots_dw, AGB, Biomass, LA_Av, LMA, LMA_lamina (NA where data unavailable or 0 for inseparable petiole).
- Dose_response_functions.csv: 6 columns including Code, POD0_J_DRF, POD1_J_DRF, POD0_P_DRF, POD1_P_DRF, AOT40_DRF (species-specific relative biomass decline per unit DO3SE POD or AOT40).
- Measurements and metadata are aligned to Ten species and nine O3 exposure regimes with consistent unit conventions; NA indicates missing data.

## Quality Control and Data Integrity
- Meteorological data validated against a local JCU meteorological station; factory-calibrated sensors used.
- O3 concentration checks performed against zero-air standards during sampling rounds.
- Final biomass measurements validated with annually calibrated scales; outliers reweighed after additional drying time.
- Documentation notes on data processing steps and modelling approaches (DO3SE, stomatal conductance parameterizations) included to support reproducibility.

## Data Access, Provenance and Use
- Data are provided with explicit documentation of data structure, parameter files, and model inputs to facilitate reuse in DGVMs or ozone-vegetation interaction studies.
- DO3SE model inputs and species-specific parameters enable recalculation or sensitivity analyses of O3 flux and phytotoxic dose assessments.
- Related literature and references cited to support interpretation of dose–response and modelling choices (e.g., Jarvis 1976; Medlyn et al. 2011; Hayes et al. 2020; CLRTAP 2017).

## References
- Key methodological and modelling references for DO3SE and stomatal conductance modelling, greenhouse/field gas exchange analyses, and phytotoxic ozone dose concepts are provided to support data interpretation and reuse.

## Data Stewardship Notes
- Ensure consistent terminology and units across derived datasets (e.g., POD metrics, LMA, AGB).
- Maintain linkages between species codes and full taxonomic information for cross-dataset interoperability.
- Preserve provenance by keeping DO3SE parameter files and input data together with derived dose–response functions.
- Be aware of limitations noted, such as hormetic responses not being accounted in the primary dose–response estimation, and the two g_s modelling approaches used for calibration.