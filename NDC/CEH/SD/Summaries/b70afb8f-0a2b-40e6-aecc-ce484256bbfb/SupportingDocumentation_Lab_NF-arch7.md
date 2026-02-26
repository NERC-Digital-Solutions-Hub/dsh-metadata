# Effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans

## Overview
- Laboratory study examining how low-dose ionising radiation affects reproduction and DNA damage in aquatic amphipods.
- Radiation exposure: phosphorus-32, dose rates of 0, 0.1, 1, and 10 mGy/d.
- Focus areas: male fertility (sperm quality and quantity), sperm viability, DNA damage in sperm, and reproductive outcomes (egg production, embryo abnormalities, and embryo size).
- Organisms studied: marine Echinogammarus marinus and freshwater Gammarus pulex.
- Data originate from the TREE project (funded by NERC, the Environment Agency and Radioactive Waste Management).

## Datasets

- Crustacean_Sperm_Data_NF.csv
  - Marine species: Echinogammarus marinus
  - Sample size: 148 individuals
  - Key variables: weight (mg); experiment number; arc-sin transformed % sperm viable; dose rate (mGy/d); fourth-root transformed sperm numbers; raw sperm numbers; raw sperm viability
  - Exposures: two separate exposures in Oct 2015 and Nov 2016
  - Data purpose: first assessment of chronic radiation effects on male fertility

- Crustacean_Sperm_Data_Freshwater.csv
  - Freshwater species: Gammarus pulex
  - Sample size: 63 individuals
  - Key variables: weight (mg); arc-sin transformed % sperm viable; dose rate (mGy/d); fourth-root transformed sperm numbers; raw sperm numbers; raw sperm viability
  - Exposure: single exposure in Aug 2016
  - Data purpose: first assessment of chronic radiation effects on male fertility

- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Marine species: Echinogammarus marinus
  - Key variables: dose rate (mGy/d); % tail DNA
  - Method: alkaline comet assay analyzed with OpenComet v1.3
  - Exposure: same dose rates as sperm datasets
  - Data purpose: assess environmentally relevant radiation-induced DNA damage in sperm

- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Cross-experiment reproduction data: exposed males mated with nonexposed females
  - Key variables: female weight (mg); number of eggs produced; time to reproduction after pairing; dose rate (mGy/d); % abnormal embryos in brood; embryo diameter (µm)
  - Data purpose: evaluate reproductive consequences (eggs and embryo quality) following paternal radiation exposure

## Methods and Measurements

- Exposure protocol: phosphorus-32 (ATP γ32P) for two weeks at 0, 0.1, 1, 10 mGy/d
- Activity assessment: HIDEX 300SL liquid scintillation counter
- Post-exposure procedures: anaesthetise, dissect testes; assess sperm counts and viability with LIVE/DEAD viability kit
- Visualization: Leica DM2000 microscope with fluorescence filters
- Sperm data: based on three replicate counts within a 5 µl sperm aliquot
- DNA damage: comet assay on sperm cells; slides processed under dark or yellow light; analysed with OpenComet v1.3
- Embryo data: females mated with exposed males; daily checks; embryos removed at standardized stage; embryos measured with ImageJ; aberrations per Sundelin & Eriksson methods

## Data Structure and Variables

- Crustacean_Sperm_Data_NF.csv
  - Columns: weight (mg), experiment number, arc-sin transformed % sperm viable, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
- Crustacean_Sperm_Data_Freshwater.csv
  - Columns: weight (mg), arc-sin transformed % sperm viable, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Columns: dose rate (mGy/d), % tail DNA
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Columns: female weight (mg), eggs produced, time to reproduction, dose rate (mGy/d), % abnormal embryos, embryo diameter (µm)

## Provenance and References
- Data collected and interpreted by Neil Fuller; interpretation supported by Prof. Alex T. Ford
- TREE project funding acknowledged (NERC, Environment Agency, Radioactive Waste Management)
- Key references for methods:
  - Gyori et al. (2014). OpenComet: automated analysis for comet assay images
  - Lacaze et al. (2011). DNA damage in freshwater amphipods as a genotoxicity tool
  - Sundelin & Eriksson (1998); Sundelin et al. (2008). Embryo aberrations as environmental stress indicators

## GIS and Data Visualization Opportunities

- Potential uses for map-based data products (GIS):
  - Visualize dose-response relationships across species and life stages; create responsive charts linking dose rate to fertility, DNA damage, and reproduction outcomes.
  - Integrate with habitat distribution data to assess vulnerability of coastal and freshwater amphipod populations to radionuclide exposure.
  - Develop risk maps showing predicted impacts on male fertility and embryonic development under different radiation scenarios, useful for regulatory and conservation planning.
- Data integration notes for GIS:
  - Datasets are lab-based with no explicit spatial coordinates; to map, relate dose-response data to field sampling sites or habitat grids via metadata or linking fields (species, exposure conditions, measured endpoints).
  - Transformations (arc-sin, fourth-root) and raw counts should be documented when visualizing or modeling to maintain interpretability.

## Considerations for Use

- Lab-based data; extrapolation to field populations requires caution.
- Sample sizes vary by dataset (e.g., 148 vs. 63 individuals); consider replication and batch effects (two exposure periods for marine data).
- Data include multiple transformations; ensure consistent handling when combining datasets for analyses.
- Datasets are designed to enable multivariate assessment of how dose rate influences sperm quality, DNA damage, and reproductive success across marine and freshwater amphipods.