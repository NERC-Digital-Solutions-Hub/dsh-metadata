# Supporting Documentation

- This collection includes four related datasets examining the effects of beta radiation (phosphorus-32) on male amphipod crustacean fertility and DNA damage, with marine and freshwater species. Data were collected in 2015–2016 under the TREE project and are described with detailed methods, structures, and provenance to support reuse and governance.

## Datasets Overview

- Crustacean_Sperm_Data_NF.csv: Marine amphipod Echinogammarus marinus; exposure to 0, 0.1, 1, 10 mGy/d; 148 individuals; covariate weight included; data on sperm numbers and viability; two separate exposures (Oct 2015, Nov 2016).
- Crustacean_Sperm_Data_Freshwater.csv: Freshwater amphipod Gammarus pulex; similar dose rates; single exposure (Aug 2016); 63 individuals; includes weight and sperm viability/counts.
- Crustacean_DNA_Damage_Sperm_Data_NF.csv: Marine E. marinus sperm DNA damage (% tail DNA) after the same radiation conditions; analyzed with OpenComet v1.3.
- Crustacean_Egg_Numbers_and_Breeding_Dates.csv: Reproductive outcomes from mating radiation-exposed males with unexposed females; includes female weight, eggs produced, time to reproduction, dose rate, % abnormal embryos, and embryo diameter.

## Dataset Details

- Crustacean_Sperm_Data_NF.csv
  - Dataset Size: 7 KB
  - Species: Echinogammarus marinus (marine)
  - Dose rates: 0, 0.1, 1, 10 mGy/d
  - Key variables: weight (mg), experiment number, arc-sin transformed % sperm viable, dose rate, fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
  - Structure: seven columns
  - Exposures: two separate experiments (Oct 2015, Nov 2016)

- Crustacean_Sperm_Data_Freshwater.csv
  - Dataset Size: 3 KB
  - Species: Gammarus pulex (freshwater)
  - Dose rates: 0, 0.1, 1, 10 mGy/d
  - Key variables: weight (mg), arc-sin transformed % sperm viable, dose rate, fourth root transformed sperm numbers, raw sperm numbers, raw sperm viability
  - Structure: six columns
  - Exposure: single exposure (Aug 2016)

- Crustacean_DNA_Damage_Sperm_Data_NF.csv
  - Dataset Size: 1 KB
  - Species: Echinogammarus marinus (marine)
  - Dose rates: 0, 0.1, 1, 10 mGy/d
  - Key variables: dose rate, % tail DNA
  - Structure: two columns
  - Analysis: alkaline comet assay; OpenComet v1.3 used for image analysis

- Crustacean_Egg_Numbers_and_Breeding_Dates.csv
  - Dataset Size: 2 KB
  - Species: Echinogammarus marinus (marine)
  - Dose rates: 0, 0.1, 1, 10 mGy/d (males exposed)
  - Key variables: female weight (mg), eggs produced, time to reproduction, dose rate, % abnormal embryos, embryo diameter (µm)
  - Structure: six columns
  - Reproduction: females mated with irradiated males; data collected after pairing and monitoring broods

## Data Provenance, Methods, and Governance

- Primary data collector: Neil Fuller; interpretation support: Professor Alex T. Ford
- Project and funding: TREE project; funded by NERC, Environment Agency, and Radioactive Waste Management
- Data collection methods: phosphorus-32 exposure via ATP γ32 P; two-week exposure; medium and organism activity measured by HIDEX 300SL; sperm counts/viability via LIVE/DEAD kit; sperm visualized with Leica microscope; DNA damage assessed via alkaline comet assay with OpenComet analysis
- Data transformations and structure: transformation applied to sperm data (arc-sin, fourth root); recorded as both raw and transformed values with explicit column definitions
- Quality and integrity notes: datasets include replicate counts (three replicates per 5 µL aliquot) and blinding for embryo measurements; metadata includes experimental dates, dosages, and measurement instruments
- Publication and citation references for methods: OpenComet (Gyori et al. 2014); DNA damage methodology (Lacaze et al. 2011); embryo abnormality measures (Sundelin & Eriksson 1998; Sundelin et al. 2008)

## Data Curation and Reuse Considerations for Data Stewards

- Ensure consistent metadata across datasets (species, dose units, exposure duration, measurement instruments, replication, transformations applied)
- Maintain clear provenance: link each dataset to the TREE project and the specific exposure dates
- Preserve data transformations and provide rationale and methods for any arcsin or fourth-root transformations in documentation
- Facilitate interoperability by harmonizing column names and units where possible (e.g., weight in mg, dose rate in mGy/d, embryo diameter in µm)
- Consider explicit data-sharing metadata and licensing to support reuse and cataloging in portals
- Note any gaps or blanks (e.g., missing data in Crustacean_Egg_Numbers_and_Breeding_Dates.csv) and document data imputation or limitations
- Ensure references and methodology are traceable to enable reproducibility and secondary analyses

## References

- Gyori, B. M., Venkatachalam, G., Thiagarajan, P. S., Hsu, D., & Clement, M. V. (2014). OpenComet: an automated tool for comet assay image analysis. Redox Biology, 2, 457-465.
- Lacaze, E., Devaux, A., Mons, R., Bony, S., Garric, J., Geffard, A., & Geffard, O. (2011). DNA damage in caged Gammarus fossarum amphipods: a tool for freshwater genotoxicity assessment. Environmental Pollution, 159(6), 1682-1691.
- Sundelin, B., & Eriksson, A. K. (1998). Malformations in embryos of the deposit-feeding amphipod Monoporeia affinis in the Baltic Sea. Marine Ecology Progress Series, 171, 165-180.
- Sundelin, B., Wiklund, A. K. E., & Ford, A. T. (2008). Biological effects of contaminants: The use of embryo aberrations in amphipod crustaceans for measuring effects of environmental stressors (Vol. 41). International Council for the Exploration of the Sea.