# Radionuclide biological half-lives for farm animals

## Overview
- Compilation of quality-controlled biological half-life values for farm animals contributing to the human food chain.
- Includes 12 animal types: cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, red grouse.
- Covers 32 radionuclides relevant to radiological protection.
- Data types include milk, muscle (meat), eggs, whole body, carcass, and various tissues (liver, kidney); additional non-food sample types (urine, faeces) are included from the same sources for modelling purposes.
- Source references are provided; dataset is part of the CONFIDENCE project within CONCERT EJP, funded under Horizon 2020.

## Data scope and collection
- Approximately 650 entries across the 12 animals and 32 radionuclides.
- Entries span multiple sample products (milk, meat, eggs, tissues) and various study conditions.
- Non-food samples present to support modelling, though not directly part of the human food chain.

## Provenance and quality
- A Microsoft Excel recording sheet was specifically designed to collate half-life values and metadata for the final dataset.
- Every source reference was consulted and data quality-controlled prior to inclusion; most entries were validated by someone other than the original entry author.
- Caution: many sources report differing numbers of loss components for the same radionuclide and product (e.g., Cs in milk with 1–5 components). This variability means means and probability distributions for a given component cannot be derived without expert interpretation.

## Metadata and structure
- Dataset uses explicit column headings and units to describe each data row. Key fields include:
  - Source_Reference, Animal, Animal_Additional_Descriptors, Age_Years, Product_Or_Tissue, Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide, Temperature_Degrees_Centigrade, Live_Weight_kg, Length_Of_Study_Days, Length_Of_Decontamination_Period_Days, Number_of_Animals, Sex, Number_Of_Meaurements_To_Determine_Biological_Half_Life, Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, Biological_Half_Life_c_Days, Biological_Half_Life_d_Days, Biological_Half_Life_e_Days, Fraction_Released_During_Process_a, Fraction_Released_During_Process_b, Fraction_Released_During_Process_c, Fraction_Released_During_Process_d, Fraction_Released_During_Process_e, Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days, Language_If_Not_English, Notes.
- Many fields may be incomplete or not information available (n/a).
- Units are specified where applicable (e.g., live weight in kilograms, temperatures in °C, times in days, milk yield in litres per day).

## Modelling and monitoring applications
- Provides a curated data foundation for radiological protection modelling and assessment of transfer of radionuclides to animal products.
- Useful for scenario analysis following radioactive contamination events (e.g., Chernobyl, Fukushima) and for evaluating policy options in environmental health monitoring.
- The dataset supports interrogation of biological half-lives across species and tissues, enabling sensitivity analyses and exploratory modelling.

## Data access, governance and barriers
- Data are sourced from a wide range of literature, including non-English and Russian/Japanese references; provenance is documented.
- Acknowledges barriers common to monitoring frameworks:
  - Data access and timely availability.
  - Silos within and between organisations.
  - Public sharing of underlying data.
  - Inadequate metadata hindering quality assessment.
  - Data transformation and standardisation efforts required for integration.
  - Need for robust data governance to ensure standards, storage, sharing, and currency.

## Limitations and caveats
- Heterogeneity in reporting across studies means direct averaging is often inappropriate; expert interpretation is required to derive best estimates or distributions for components of loss.
- Not all data fields are filled for every entry; uncertainty and gaps must be managed in analyses and dashboards.
- Some data originate from older or locale-specific studies; cross-context applicability should be evaluated.

## Relevance to monitoring frameworks
- Aligns with the aim of identifying environmental health measures to scrutinise policy and inform future decisions.
- Demonstrates practical considerations for building and maintaining a monitoring data base: data curation, metadata richness, provenance, validation, and governance.
- Highlights the importance of openness and data management practices to enable transparent decision-making and evidence-based policy.

## References
- The dataset includes an extensive reference list of source studies (examples span from the 1950s to the 2010s, across multiple countries and languages), all of which are cited within the data records to support provenance and traceability.