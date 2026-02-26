Radionuclide biological half-lives for farm animals

## Overview
- A quality-controlled compilation of biological half-life values (and related information) for farm animals that contribute to the human food chain.
- ~650 data entries across 12 animal types: cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, red grouse.
- Covers 32 radionuclides/elements relevant to radiological protection.
- Data include values for milk, muscle, eggs, whole body, carcass, and various tissues (e.g., liver, kidney); additional sample types (urine, faeces) are included when reported in the same source.
- Source references are provided for all entries.
- Part of the CONFIDENCE project, under CONCERT EJP, funded by the EU Horizon 2020 programme (grant No 662287).

## Provenance & Quality
- Data assembled using a dedicated Excel recording sheet to collate half-life values and associated information for the final dataset.
- Each source reference consulted and data quality-controlled; most entries validated by someone other than the original entry creator.
- Caution: source references often report different numbers of loss components for the same nuclide/product (e.g., Cs in milk may have 1–5 components). This means:
  - It is not appropriate to simply derive universal means or probability distributions for a given component.
  - Users may need to interpret and select component(s) to derive a best estimate.

## Data Schema and Columns
- The dataset is tabular with explicit column headings and units where applicable. Key columns include:
  - Source_Reference, Language_If_Not_English
  - Animal, Animal_Additional_Descriptors, Age_Years, Live_Weight_kg
  - Product_Or_Tissue, Stage_Of_Lactation_Days
  - Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide
  - Temperature_Degrees_Centigrade, Length_Of_Study_Days, Number_of_Animals, Sex
  - Number_Of_Meaurements_To_Determine_Biological_Half_Life
  - Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, Biological_Half_Life_c_Days, Biological_Half_Life_d_Days, Biological_Half_Life_e_Days
  - Fraction_Released_During_Process_a, Fraction_Released_During_Process_b, Fraction_Released_During_Process_c, Fraction_Released_During_Process_d, Fraction_Released_During_Process_e
  - Notes
  - Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days
- Many fields use Not Applicable (n/a) where information is not available.
- Units where applicable: Live_Weight_kg (kg, fresh mass), Temperature_Degrees_Centigrade (°C), Milk_Yield_Litres_Per_Day (L/day), Biological_Half_Life_*_Days (days), Length_Of_Study_Days (days), etc.
- The dataset explicitly notes that not all rows will have complete fields; the structure supports cross-linking animal type, product, radionuclide, and study details.

## Use and Purpose for Modelling
- Designed to support radiological protection modelling and data-driven exploration of radionuclide transfer to human food chains.
- Enables self-serve analysis and dashboard-style outputs for end users to compare biological half-lives across animals, products, and radionuclides.
- Facilitates combining with other datasets or expert input to derive best-estimate values for modelling and risk assessment.
- The inclusion of original references supports traceability and validation of results.

## Limitations and Guidance for Use
- Differences in reported loss components across sources mean users must carefully interpret which components to include for a given scenario.
- Deriving universal means or probability distributions from the compiled values is not straightforward; expert interpretation is often required.
- The dataset is best used as a reference library for parameter values, with explicit documentation of chosen components and assumptions for any modelling output.

## References and Source Coverage
- Contains an extensive list of source references used to populate the entries (encompassing historical and contemporary studies).
- References include a broad range of languages and publications (including Russian sources), illustrating the historical breadth of radionuclide transfer research in farm animals.
- Each data row is linked to its source reference to support traceability and reproducibility.

## Project Context and Access
- Created as part of the CONFIDENCE project, within the CONCERT EJP framework.
- Funded by the European Union’s Horizon 2020 Research and Innovation Programme (grant No 662287).
- Designed to be a robust, citable data resource for researchers and practitioners needing reliable biological half-life parameters for farm animals.