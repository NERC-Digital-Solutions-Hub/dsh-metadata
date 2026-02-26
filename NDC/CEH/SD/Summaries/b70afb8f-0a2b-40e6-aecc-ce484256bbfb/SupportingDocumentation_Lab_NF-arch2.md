# Supporting Documentation

## Overview
- Compiles datasets examining the effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans.
- Aims to provide the first assessment of chronic radiation exposure impacts on male fertility and DNA damage in aquatic invertebrates.
- Part of the TREE project funding (NERC, Environment Agency, Radioactive Waste Management).

## Datasets and Content
- Crustacean_Sperm_Data_NF.csv (marine: Echinogammarus marinus)
  - Dose rates: 0, 0.1, 1, 10 mGy/d; two-week exposure.
  - 148 individuals; includes weight as a covariate.
  - Columns: weight (mg), experiment number, arc-sin transformed % sperm viable, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability (% live/total).
- Crustacean_Sperm_Data_Freshwater.csv (freshwater: Gammarus pulex)
  - Dose rates: 0, 0.1, 1, 10 mGy/d; single exposure in August 2016.
  - 63 individuals; weight included as a covariate.
  - Columns: weight (mg), arc-sin transformed % sperm viable, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability.
- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - DNA damage in sperm after radiation exposure; % tail DNA from alkaline comet assay.
  - Dose rates: 0, 0.1, 1, 10 mGy/d; November 2016 data collection.
  - Columns: dose rate (mGy/d), % tail DNA.
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Reproduction outcomes when radiation-exposed males mate with nonexposed females.
  - Columns: female weight (mg), eggs produced per brood, time to reproduction after male addition, dose rate (mGy/d), % abnormal embryos, embryo diameter (µm).

## Methods and Measurements
- Radiation exposure: phosphorus-32 (ATP γ32 P) source.
- Dose assessment: HIDEX 300SL liquid scintillation counter for activity in exposure medium and organisms.
- Sperm assessment: LIVE/DEAD sperm viability kit; fluorescence microscopy (Leica DM2000) with specified filters.
- DNA damage: alkaline comet assay; OpenComet v1.3 for image analysis; detailed protocol including slide preparation and staining.
- Embryo assessment: embryos removed from brood pouch, imaged and measured (ImageJ); blind analysis for embryo data.

## Study Design and Timeline
- Marine exposures: two separate rounds in Oct 2015 and Nov 2016; two-week exposure periods.
- Freshwater exposure: single two-week exposure in Aug 2016.
- Reproductive outcomes measured after exposure by pairing exposed males with unexposed females; daily checks and standardized timing for embryo assessment.

## Data Structure and Quality
- Each dataset has clearly defined columns with documented transformations (arc-sine, fourth root).
- Data collected and curated by Neil Fuller; interpretation supported by Alex T. Ford.
- Data generated under the TREE project; intended for environmental monitoring and genotoxicity assessment.
- Quality controls noted, including blinded embryo photography to reduce bias.

## Data Provenance and Stewardship
- All data collection and interpretation performed by a named researcher (Neil Fuller) with collaboration from Project participants.
- Data described as first assessments of chronic radiation effects on selected aquatic invertebrates.
- Related references provided for methods (OpenComet, comet assay procedures, and embryo abnormality analysis).

## Relevance for Environmental Monitoring
- Provides standardized, multi-faceted endpoints (sperm quality and quantity, DNA damage, and reproductive success) under controlled low-dose radiation exposure.
- Datasets are suitable for integration with other monitoring data to evaluate environmental health and policy performance over time.
- Emphasizes data transparency, reproducible methods, and storage/availability of underlying data for broader access and reuse.