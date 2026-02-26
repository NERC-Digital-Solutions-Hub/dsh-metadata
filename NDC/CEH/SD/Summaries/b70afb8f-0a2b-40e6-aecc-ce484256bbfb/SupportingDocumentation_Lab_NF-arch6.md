# Supporting Documentation

- This document describes four datasets and their collection methods related to the effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans, plus references and data provenance.

## Overview of purpose and scope
- First assessment of chronic radiation effects on male fertility and DNA damage in aquatic invertebrates.
- Datasets include sperm quality and quantity, DNA damage (tail DNA), and reproductive outcomes (egg production and embryo abnormalities) following phosphorus-32 beta radiation.
- Data collected under the TREE project (funded by NERC, the Environment Agency, and Radioactive Waste Management).

## Datasets

### Crustacean_Sperm_Data_NF.csv (Marine: Echinogammarus marinus)
- Dataset size: 7 KB
- Purpose: Assess impacts of chronic radiation on male fertility in a marine amphipod.
- Dose rates: 0, 0.1, 1, 10 mGy/d
- Sample size: 148 individuals
- Covariate: weight (mg)
- Data columns:
  - weight (mg)
  - experiment number
  - arc-sin transformed % sperm viable
  - dose rate (mGy/d)
  - fourth root transformed sperm numbers
  - raw sperm numbers
  - raw sperm viability (live/dead x 100)
- Methods highlights:
  - Two-week exposure to phosphorus-32
  - HAR: HIDEX 300SL for activity
  - Sperm counts and viability via LIVE/DEAD kit
  - Sperm suspensions viewed with a Leica fluorescence microscope
  - Three replicate counts within a 5 µl aliquot

### Crustacean_Sperm_Data_Freshwater.csv (Freshwater: Gammarus pulex)
- Dataset size: 3 KB
- Purpose: Assess impacts of chronic radiation on male fertility in a freshwater amphipod.
- Dose rates: 0, 0.1, 1, 10 mGy/d
- Sample size: 63 individuals
- Covariate: weight (mg)
- Data columns:
  - weight (mg)
  - arc-sin transformed % sperm viable
  - dose rate (mGy/d)
  - fourth root transformed sperm numbers
  - raw sperm numbers
  - raw sperm viability (live/dead x 100)
- Methods highlights:
  - One exposure in August 2016
  - Similar exposure, measurement, and analysis workflow as marine dataset

### Crustacean_DNA_Damage_Sperm_Data_NF.csv
- Dataset size: 1 KB
- Purpose: Assess environmentally relevant radiation-induced DNA damage in sperm.
- Dose rates: 0, 0.1, 1, 10 mGy/d
- Data columns:
  - dose rate (mGy/d)
  - % tail DNA
- Methods highlights:
  - Alkaline comet assay performed on exposed sperm
  - OpenComet v1.3 used for image analysis
  - Slides prepared and processed under controlled lighting to avoid additional DNA damage

### Crustacean_Egg_Numbers_and_Breeding_Dates.csv
- Dataset size: 2 KB
- Purpose: Evaluate reproductive outcomes after exposure; breeding with nonexposed females.
- Dose rates: 0, 0.1, 1, 10 mGy/d (males exposed)
- Data columns:
  - female weight (mg)
  - eggs produced by females breeding with exposed males
  - time to reproduction after male addition
  - dose rate (mGy/d)
  - % abnormal embryos in brood
  - embryo diameter (µm)
- Methods highlights:
  - Post-exposure mating with unexposed females
  - Daily checks; embryos removed after five days
  - Embryos imaged and measured with ImageJ
  - Random blind coding of photographs for analysis

## Data collection and provenance
- Primary data collector: Neil Fuller; interpretation support from Alex T. Ford
- Funding: TREE project; NERC, Environment Agency, Radioactive Waste Management
- Data structure notes:
  - Marine and freshwater sperm datasets include transformed metrics to support statistical analyses
  - DNA damage dataset uses a two-column format (dose rate and % tail DNA)
  - Reproduction dataset links male exposure dose to offspring outcomes and embryo abnormalities

## References
- Gyori, B. M. et al. OpenComet: automated comet assay image analysis. Redox Biology, 2014.
- Lacaze, E. et al. DNA damage in caged Gammarus fossarum amphipods. Environmental Pollution, 2011.
- Sundelin, B. & Eriksson, A. K. E. Malformations in embryos of amphipods. Marine Ecology Progress Series, 1998.
- Sundelin, B. et al. Use of embryo aberrations in amphipods for assessing environmental stressors. ICES, 2008.

## How this supports data use and product creation
- Enables cross-dataset dose-response analyses linking sperm quality, DNA damage, and reproductive outcomes.
- Covariate data (weight) allows normalization and adjustment in analyses.
- Clear metadata on data collection methods, units, and transformations supports data quality checks and reproducibility.
- Potential for dashboards and self-serve analyses combining sperm, DNA damage, and breeding data, with appropriate filters for species and dose rate.