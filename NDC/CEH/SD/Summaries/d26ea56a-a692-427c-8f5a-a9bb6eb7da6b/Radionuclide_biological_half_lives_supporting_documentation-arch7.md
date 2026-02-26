# Radionuclide biological half-lives for farm animals

## Overview
- A quality-controlled compilation of biological half-life values for radionuclides in farm animals, aimed at supporting radiological protection modelling and data visualisation.
- About 650 entries covering 12 animal types: cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, and red grouse.
- Includes data for human food chain products (milk, muscle/meat, eggs, whole body, carcass, and tissues such as liver and kidney) and additional sample types (e.g., urine, faeces) that appear in sources but may still inform modelling.
- Encompasses 32 radionuclides/elements relevant to radiological protection.
- Data collected as part of the CONFIDENCE project within the CONCERT EJP, funded by the EU Horizon 2020 programme.

## Content and structure relevant to GIS
- Each data row can include: Source_Reference, Animal, Animal_Additional_Descriptors, Age_Years, Product_Or_Tissue, Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide, Temperature_Degrees_Centigrade, Live_Weight_kg, Length_Of_Study_Days, Length_Of_Decontamination_Period_Days, Number_of_Animals, Sex, Number_Of_Meaurements_To_Determine_Biological_Half_Life, Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, Biological_Half_Life_c_Days, Biological_Half_Life_d_Days, Biological_Half_Life_e_Days, Fraction_Released_During_Process_a/b/c/d/e, Notes, Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days, Language_If_Not_English.
- Units are specified where applicable; many fields may be missing for individual rows.
- The dataset includes a comprehensive References field, citing primary sources for each entry.

## Data quality and provenance
- Data recorded via a designed Excel sheet to facilitate collation into the final dataset.
- Each source reference was consulted and data quality-controlled; most entries validated by someone other than the initial entry author.
- Important caveat: source references often report different numbers of loss components for the same radionuclide-tissue combination (e.g., Cs in milk), so straightforward means or probability distributions cannot be derived without interpretation.

## GIS-oriented considerations and potential uses
- Not inherently spatial, but highly suitable for map-based data products when combined with spatial exposure data (e.g., farm locations, contamination maps).
- Can be used to create layers by animal type, radionuclide, tissue/product, and biokinetic component (via half-lives and fractions released), enabling scenario visualisations and risk mapping.
- Useful for parameterising dynamic transfer models across space (e.g., regional livestock inventories, grazing patterns, and contamination plumes).

## Limitations and caveats
- Coverage is uneven across animal types and radionuclides; some elements/products have abundant entries, others are sparse.
- Mixed reporting across studies (different numbers of loss components) complicates synthesis into single estimates.
- Some sources are non-English (e.g., Russian, Japanese, others), which may affect translation and interpretation.
- The dataset includes data not strictly for human food products, but potentially informative for modelling the broader transfer processes.

## Access, scope, and references
- The dataset consolidates references from a wide range of studies (historical and contemporary) and provides full provenance for each entry.
- Scope reflects radiological protection interests and supports both modelling and data-sharing objectives within the CONFIDENCE/CONCERT context.