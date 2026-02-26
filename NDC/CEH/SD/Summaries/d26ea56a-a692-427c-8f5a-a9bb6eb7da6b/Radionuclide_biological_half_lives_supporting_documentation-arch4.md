# Radionuclide biological half-lives for farm animals

## Overview
- A quality-controlled dataset of biological half-life values for radionuclides in farm animals that contribute to the human food chain.
- Contains approximately 650 entries across 12 animal types (cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, red grouse) and 32 radionuclides/elements relevant to radiological protection.
- Entries cover human food chain products (milk, muscle/meat, eggs, whole body, carcass, and specific tissues) and additional sample types (urine, faeces, etc.) reported in same sources for potential modelling use.
- Part of the CONFIDENCE project within the CONCERT European Joint Programme (EJP), funded by EU Horizon 2020 (grant No 662287).

## Data content at a glance
- Approximately 650 data entries for biological half-lives, including single and multiple components of loss (e.g., first to fifth components where reported).
- Products/Tissues include milk yields, meat/muscle, eggs, organ/tissue data (liver, kidney, etc.), and whole-body measurements.
- Metadata fields cover: animal, age, live weight, contamination route, source of radionuclide, study type, temperature, study duration, number of animals, sex, measurement counts, and notes.
- Includes both human-food related data and non-food sample types linked to the same references for potential modelling use.
- The dataset provides extensive references for traceability of all data points.

## Provenance and quality
- Data collected using a purpose-built recording sheet (Excel) designed to collate half-life values and associated information into the final dataset.
- Each source reference was reviewed and data quality-controlled prior to inclusion; most entries have been quality-checked by someone other than the entry author.
- Caution: source references often report different numbers of loss components for the same compound and food product, making it difficult to derive simple means or distributions without interpretation.

## Data schema and metadata
- Key columns and their purposes (examples):
  - Source_Reference: citation for data source.
  - Animal / Animal_Additional_Descriptors: species and extra details.
  - Age_Years, Live_Weight_kg, Temperature_Degrees_Centigrade: contextual physiological/experimental conditions.
  - Product_Or_Tissue: target product or tissue (e.g., milk, muscle, eggs).
  - Radionuclide / Element: isotope and element involved.
  - Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, etc.: recorded half-lives, including multiple components when reported.
  - Length_Of_Study_Days, Length_Of_Decontamination_Period_Days: study duration and decontamination intervals.
  - Number_of_Animals, Sex, Study_Type, Contamination_Route, Source_Of_Radionuclide: experimental design and context.
  - Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day: production data linked to milk studies.
  - Language_If_Not_English, Notes: contextual and methodological notes.
- A comprehensive list of column explanations is provided, including units and when information is not available (n/a).

## Provenance, trust, and limitations
- All source references are included to enable traceability and reproducibility.
- Data quality control acknowledges variability across sources, especially for the number and interpretation of loss components; users should apply expert judgment when deriving best estimates or comparative analyses.
- Some fields are incomplete or not applicable in certain rows (n/a), reflecting the heterogeneity of historical data.

## Use cases for data leaders
- Data strategy and governance
  - Treat this dataset as a research-grade data asset with clear provenance, quality steps, and metadata to support trustworthy analyses.
  - Establish data stewardship and versioning to manage updates or new references.
  - Document data lineage and decisions when deriving composite estimates from multiple loss components.
- Data discovery and access
  - Ensure discoverability by cataloging the dataset with its metadata schema, source references, and data quality notes.
  - Facilitate cross-network collaboration by providing access to both food-chain products and related non-food sample types for modelling.
- Data quality and standards
  - Address variability in loss component reporting by developing guidance on interpreting multi-component half-lives.
  - Promote standardization of metadata fields (e.g., age, weight, temperature, study type) to improve comparability across studies.
- Modelling and decision support
  - Use the dataset to support radiological protection modelling of radionuclide transfer to animal products and human exposure assessment.
  - Identify data gaps (e.g., granularity or specific animal/product combinations) to prioritise targeted data gathering.
- Collaboration and communities of practice
  - Leverage the broad, multi-source nature of the data to foster cross-institutional collaborations for data enrichment and validation.

## Context and funding
- Created as part of the CONFIDENCE project within the CONCERT EJP initiative.
- Funded by the European Union’s Horizon 2020 Research and Innovation Programme (grant No 662287).

## References and sources
- Extensive list of source publications spanning multiple decades and languages (English, Russian, Japanese, etc.), detailing transfer, metabolism, and biological half-lives of radionuclides in a wide range of farm animals.