# Radionuclide biological half-lives for farm animals

## Scope and content
- Compilation of quality-controlled biological half-life values (and associated information) from literature for animals that contribute to the human food chain.
- Approximately 650 entries covering 12 animal types: cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, and red grouse.
- 32 elements relevant to radiological protection.
- Entries include values for milk, muscle (meat), eggs, whole body, carcass and various tissues (e.g., liver, kidney).
- Includes other sample types (urine, faeces, etc.) not always linked to human food but appearing in the same source references; may be useful for modelling.
- All source references are provided.
- Part of the CONFIDENCE project, within CONCERT EJP, funded by the European Union’s Horizon 2020 programme (grant No 662287).

## Provenance and quality
- A recording sheet (Excel) was designed to collate half-life values and related information into the final dataset.
- Each source reference was consulted and data quality-controlled before inclusion.
- The majority of entries have been validated by someone other than the original entry author.
- Caution: source references often report differing numbers of loss components (e.g., for Cs in milk, reports range from one to five components). This makes deriving simple means or probability distributions for a given component inappropriate without careful interpretation.

## Data structure and metadata
- Extensive column headings with explicit units (examples):
  - Source_Reference, Animal, Age_Years, Product_Or_Tissue, Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide, Temperature_Degrees_Centigrade, Live_Weight_kg, Length_Of_Study_Days, Number_of_Animals, Sex, Number_Of_Meaurements_To_Determine_Biological_Half_Life, Biological_Half_Life_Single_Days, Biological_Half_Life_a_Days, Biological_Half_Life_b_Days, Biological_Half_Life_c_Days, Biological_Half_Life_d_Days, Biological_Half_Life_e_Days, Fraction_Released_During_Process_a, Fraction_Released_During_Process_b, Fraction_Released_During_Process_c, Fraction_Released_During_Process_d, Fraction_Released_During_Process_e, Notes, Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days, Language_If_Not_English.
- Many fields may be listed as not information available (n/a); units include days, kilograms, degrees Celsius, litres per day, etc.
- Rich provenance enables traceability back to original source references (full reference list included).

## Data governance, usage, and maintenance
- Dataset designed to support radiological protection modelling and research; the modelling must account for multiple loss components and avoid simplistic averaging.
- Data stewards’ practices encouraged: document data handling, provide guidance/tools to data creators to ensure standards in accuracy, metadata, and format; plan for updates and clearly note limitations.
- The dataset’s structure supports uploading to relevant data portals and catalogues, with accompanying metadata and notes to facilitate discoverability and reuse.
- Given the range of sources and languages, proper citation and context from the original references are essential for correct interpretation.

## Practical guidance for users
- Interpret biological half-life values with care when multiple loss components exist; avoid deriving single mean estimates without considering component structure.
- Leverage the detailed metadata (animal, product/tissue, age, study type, contamination route, temperature, etc.) to align data with specific modelling scenarios.
- Use the Notes field and the provided references to understand context and any study-specific assumptions or limitations.

## References and provenance context
- The dataset references numerous studies and reports dating from the 1960s to 2010s, including work related to Chernobyl and Fukushima fallout.
- The work is prepared within the CONFIDENCE project framework, contributing to harmonised data curation for radiological protection.