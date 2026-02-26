# Radionuclide biological half-lives for farm animals

## Overview
- A quality-controlled dataset compiling biological half-life values for radionuclides in farm animals, contributing to the human food chain.
- Contains ~650 entries across 12 animal types (cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, red grouse) and 32 elements relevant to radiological protection.
- Data cover milk, muscle, eggs, whole body, carcass, and various tissues; includes additional sample types (e.g., urine, faeces) from the same sources for modelling purposes.
- Part of the CONFIDENCE project within the CONCERT EJP, funded by the EU Horizon 2020 programme.

## Data Content
- Entries describe transfer and biological half-lives for radionuclides in different food-chain products and tissues.
- The number of entries per element/food product varies considerably.
- Some non-food samples are included to support modelling, though not directly tied to human food products.
- Source references are fully provided to support traceability.

## Provenance & Quality
- Review started with a designed Excel recording sheet to collate half-life values and related data into a final dataset.
- All source references are consulted and data quality-controlled prior to inclusion; most entries are validated by someone other than the original entry creator.
- Users should be cautious when summarising values because many sources report different numbers of loss components (e.g., Cs in milk may have 1–5 components), making simple means or single distributions inappropriate without interpretation.

## Dataset Structure and Variables
- Core fields (example): Source_Reference, Animal, Animal_Additional_Descriptors, Age_Years, Product_Or_Tissue, Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide, Temperature_Degrees_Centigrade, Live_Weight_kg, Length_Of_Study_Days, Length_Of_Decontamination_Period_Days, Number_of_Animals, Sex, Number_Of_Meaurements_To_Determine_Biological_Half_Life, Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, Biological_Half_Life_c_Days, Biological_Half_Life_d_Days, Biological_Half_Life_e_Days, Fraction_Released_During_Process_a, Fraction_Released_During_Process_b, Fraction_Released_During_Process_c, Fraction_Released_During_Process_d, Fraction_Released_During_Process_e, Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days, Language_If_Not_English, Notes.
- Includes multiple components of biological half-life (a, b, c, d, e) and corresponding fractions of release where reported.
- Additional variables capture experimental context (temperature, weight, study duration), production type (milk, meat, eggs), and lactation stage.
- The dataset references a long list of source publications (historical and contemporary, many in Russian and Japanese), enabling traceable provenance.

## Use and Limitations
- Designed for environmental health and radiological protection analyses, enabling transfer modelling from feed to animal products and human exposure assessments.
- Useful for comparing across species, products, and radionuclides, and for feeding into dynamic transfer models.
- Limitations include variability in reported components of loss, incomplete data for some entries, and the need for interpretation when deriving “best estimates” or distributions from heterogeneous sources.

## Provenance & Access
- Funded as part of CONFIDENCE (within CONCERT EJP) and supported by the EU Horizon 2020 programme (No. 662287).
- All data points are traceable to cited references; the dataset emphasizes quality control and documentation to support reliable environmental monitoring analyses.

## Implications for Monitoring and Data Sharing
- Provides a standardized, quality-controlled repository of biological half-life values to support consistent environmental health assessments over time.
- Highlights the value of linking this dataset with other environmental data to enhance usefulness beyond single-use applications.
- Encourages open access to underlying data sources to enable reproducibility and broader scrutiny by policymakers and researchers.