# Supporting Documentation Effects of low-dose ionising radiation on reproduction and DNA damage in marine and freshwater amphipod crustaceans

## Overview
- Organization of data documenting the effects of chronic low-dose radiation on reproductive biology and DNA integrity in aquatic amphipods.
- Species included: marine Echinogammarus marinus and freshwater Gammarus pulex.
- Exposures: phosphorus-32 beta radiation at dose rates of 0, 0.1, 1, and 10 mGy/d.
- Data collected across two exposures for marine (October 2015) and freshwater (August 2016) datasets; additional sperm DNA damage dataset from November 2016.
- Primary purpose: provide first assessments of consequences of chronic radiation exposure on male fertility and DNA damage in these aquatic invertebrates, generated under the TREE project (funded by NERC, Environment Agency, and Radioactive Waste Management).

## Datasets
- Crustacean_Sperm_Data_NF.csv
  - Marine species: Echinogammarus marinus
  - Size: 7 KB
  - Data: sperm quality and quantity; includes weight and 148 individuals across exposures
- Crustacean_Sperm_Data_Freshwater.csv
  - Freshwater species: Gammarus pulex
  - Size: 3 KB
  - Data: sperm quality and quantity; includes weight and 63 individuals
- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Marine species: Echinogammarus marinus
  - Size: 1 KB
  - Data: DNA damage in sperm (percent tail DNA) via comet assay; from November 2016
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Marine species: Echinogammarus marinus
  - Size: 2 KB
  - Data: reproductive outcomes after mating exposed males with unexposed females; includes eggs produced, reproduction timing, and embryo abnormalities

## Data collection and processing methods
- Exposure protocol:
  - Phosphorus-32 from ATP γ32 P used to expose individuals for two weeks at 0, 0.1, 1, 10 mGy/d.
  - Exposure medium and organism activity concentrations measured with HIDEX 300SL counter.
- Sperm assessment:
  - Post-exposure, testes dissected; sperm counts and viability measured with LIVE/DEAD sperm viability kit.
  - Visualization via Leica DM2000 fluorescence microscope; measurements based on three replicates within a 5 μL sperm aliquot.
- DNA damage assessment (marine sperm cells):
  - Alkaline comet assay performed; OpenComet v1.3 used for analysis.
  - Steps included cell lysis, electrophoresis, neutralization, staining with SYBR Gold, imaging, and blind analysis.
- Reproductive outcome (egg numbers and breeding dates):
  - Males exposed to radiation mated with non-exposed females; time to reproduction recorded.
  - Embryos were examined post-breeding; percent abnormal embryos and embryo diameters measured (ImageJ).
- Data collection leadership:
  - All data collected and interpreted by Neil Fuller; interpretation supported by Professor Alex T. Ford.
  - TREe project funding acknowledged.

## Data structure and metadata
- Crustacean_Sperm_Data_NF.csv
  - Columns: weight (mg), experiment number, arc-sin transformed % viable sperm, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
- Crustacean_Sperm_Data_Freshwater.csv
  - Columns: weight (mg), arc-sin transformed % viable sperm, dose rate (mGy/d), fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Columns: dose rate (mGy/d), % tail DNA
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Columns: female weight (mg), eggs produced, time to reproduction, dose rate (mGy/d), % abnormal embryos, embryo diameter (μm)

## Provenance and purpose
- Data generated under the TREE project; funded by NERC, the Environment Agency, and Radioactive Waste Management.
- Primary aim: provide the first assessment of chronic radiation exposure effects on male fertility and DNA damage in aquatic amphipods.
- Data steward: Neil Fuller; analytical interpretation aided by Alex T. Ford.

## Implications for data leadership and governance
- Data assets span multiple related datasets; ensure unified metadata standards and consistent units across datasets.
- Maintain traceable data provenance, including exposure conditions, species, and timing to support reproducibility and cross-study synthesis.
- Encourage co-ownership and collaboration across teams to align data products with user needs (e.g., environmental risk assessors, policy colleagues).
- Consider data quality aspects: small sample sizes per exposure, two separate studies, and transformation steps (arc-sin, fourth root) that should be clearly documented in any downstream analyses.
- Plan for long-term discoverability and interoperability by linking dataset descriptions to publications and including clear data structure definitions and transformation notes.

## References
- Gyori, B. M., Venkatachalam, G., Thiagarajan, P. S., Hsu, D., & Clement, M. V. (2014). OpenComet: an automated tool for comet assay image analysis. Redox biology, 2, 457-465.
- Lacaze, E., Devaux, A., Mons, R., Bony, S., Garric, J., Geffard, A., & Geffard, O. (2011). DNA damage in caged Gammarus fossarum amphipods: a tool for freshwater genotoxicity assessment. Environmental Pollution, 159(6), 1682-1691.
- Sundelin, B., Eriksson, A. K., & others (1998). Malformations in embryos of the deposit-feeding amphipod Monoporeia affinis in the Baltic Sea. Marine Ecology Progress Series, 171, 165-180.
- Sundelin, B., Wiklund, A. K. E., & Ford, A. T. (2008). Biological effects of contaminants: The use of embryo aberrations in amphipod crustaceans for measuring effects of environmental stressors. ICES Journal.