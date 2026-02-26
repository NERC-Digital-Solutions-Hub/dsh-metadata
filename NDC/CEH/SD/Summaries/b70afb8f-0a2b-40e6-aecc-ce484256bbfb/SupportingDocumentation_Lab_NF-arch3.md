# Effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans

## Overview
- Examines effects of chronic low-dose beta radiation (phosphorus-32) on male fertility, DNA damage, and reproductive outcomes in aquatic amphipods.
- Species studied: marine Echinogammarus marinus and freshwater Gammarus pulex.
- Dose rates: 0, 0.1, 1, and 10 mGy/d; exposures typically two weeks.
- Endpoints include sperm counts and viability, DNA damage in sperm, and reproduction metrics (eggs produced, time to reproduction, embryo abnormalities, embryo size).
- Data generated under the TREE project funded by NERC, the Environment Agency, and Radioactive Waste Management.

## Datasets and key variables
- Crustacean_Sperm_Data_NF.csv (marine)
  - 148 individuals; seven columns: weight (mg), experiment number, arc-sin transformed % viable sperm, dose rate (mGy/d), fourth-root transformed sperm numbers, raw sperm numbers, raw sperm viability (%).
  - Purpose: first assessment of chronic radiation effects on male fertility; two-week exposure in October 2015.
- Crustacean_Sperm_Data_Freshwater.csv (freshwater)
  - 63 individuals; six columns: weight (mg), arc-sin transformed % viable sperm, dose rate (mGy/d), fourth-root transformed sperm numbers, raw sperm numbers, raw sperm viability.
  - Purpose: same objective for Gammarus pulex; single exposure in August 2016.
- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Two columns: dose rate (mGy/d) and % tail DNA in sperm (DNA damage) using alkaline comet assay; OpenComet v1.3 analysis.
  - Purpose: first assessment of environmentally relevant radiation doses on DNA damage in crustacean sperm; November 2016 data.
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Six columns: female weight (mg), number of eggs produced with exposed male, time to reproduction after pairing, dose rate (mGy/d), % abnormal embryos in brood, embryo diameter (µm).
  - Purpose: assess reproductive consequences (eggs, timing, abnormalities) after mating with radiation-exposed males; blind analysis conducted.

## Methods and data collection context
- Exposure to phosphorus-32 (ATP γ32P) for two weeks across all datasets; dose rates of 0, 0.1, 1, 10 mGy/d.
- Measurements:
  - Sperm counts and viability via LIVE/DEAD sperm viability kit; counts from three replicates per 5 µl sample; visualization with fluorescence microscopy.
  - DNA damage assessment via comet assay; slides prepared under controlled conditions and analyzed with OpenComet.
  - Reproductive outcomes obtained by pairing exposed males with non-exposed females, monitoring for ovigerous reproduction, and measuring eggs, timing, embryo abnormalities, and embryo size. Analyses performed blind where indicated.
- Data management and transformations:
  - Sperm data include arc-sin and fourth-root transformations to stabilize variance; raw counts and viability provided for transparency.
  - Data structures described per dataset (number of columns and types).

## Purpose and relevance for monitoring frameworks
- Provides multi-level environmental health measures linking:
  - Individual-level endpoints: sperm quality, quantity, and DNA integrity.
  - Population-level endpoints: reproduction timing, fecundity, and embryo abnormalities.
- Enables dose-response assessment for chronic low-dose radiation in aquatic invertebrates and cross-species comparisons (marine vs freshwater).
- Supports evidence-based policy evaluation and monitoring of environmental genotoxic stress and reproductive viability, particularly where radiological exposures may affect aquatic ecosystems.

## Data provenance, governance, and accessibility
- Collected and interpreted by Neil Fuller; collaboration with Alex T. Ford; data generated under the TREE project.
- Funding: NERC, Environment Agency, and Radioactive Waste Management.
- Data format is dataset-specific CSV files with clearly defined variables and metadata within each entry; some datasets include data transformations and citations for analytical tools (e.g., OpenComet).

## Implications and considerations for monitoring practice
- Useful as a template for monitoring frameworks to capture:
  - Endpoints across biological organization levels (molecular to population).
  - Dose-response relationships and cross-species comparisons.
  - Transparent data processing, including explicit transformations and sharing of raw data.
- Practical considerations for policy use:
  - Metadata completeness and standardization across datasets to reduce barriers in data sharing and integration.
  - Open accessibility of underlying data while ensuring appropriate data governance.
  - Clarity on the applicability of laboratory-based radiation exposure to environmental contexts.
- Limitations to consider in policy translation:
  - Lab-based exposure scenarios may not replicate environmental complexity.
  - Sample sizes are modest, which may affect generalizability.
  - Temporal gaps between marine and freshwater datasets.

## References
- Gyori, B. M., et al. OpenComet: automated tool for comet assay image analysis. Redox Biology, 2014.
- Lacaze, E., et al. DNA damage in caged Gammarus fossarum amphipods. Environmental Pollution, 2011.
- Sundelin, B., Eriksson, A. K. E. Embryo aberrations as indicators of environmental stressors. ICES, 1998; Sundelin, et al. 2008.