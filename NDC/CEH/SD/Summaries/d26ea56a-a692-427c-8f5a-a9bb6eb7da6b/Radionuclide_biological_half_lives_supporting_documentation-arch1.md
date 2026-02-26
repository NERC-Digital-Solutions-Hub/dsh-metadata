# Radionuclide biological half-lives for farm animals

- Aim and scope
  - A quality-controlled compilation of biological half-life values for radionuclides in farm animals contributing to the human food chain.
  - Almost 650 entries covering 12 animal types: cattle, sheep, goats, deer, geese, hens, horses, pigs, rabbits, camels, ducks, and red grouse.
  - Includes 32 elements relevant to radiological protection.
  - Data types include milk, muscle (meat), eggs, whole body, carcass, and various tissues (e.g., liver, kidney); also other sample types (urine, faeces) present in the same source references for modelling purposes.
  - Source references are provided; part of the CONFIDENCE project within CONCERT EJP, funded by the EU Horizon 2020 programme.

- Provenance and quality
  - Data were gathered using a purpose-built Excel recording sheet to collate half-life values and associated information.
  - Each source was consulted and data quality-controlled before inclusion; the majority of entries were quality-checked by someone other than the entry author.
  - Users should be cautious when summarising, because sources often report differing numbers of loss components (e.g., Cs in milk may have 1 to 5 components), making it difficult to derive simple means or probability distributions for a given component.
  - The dataset provides the raw entries and notes to support careful interpretation rather than definitive statistical summaries.

- Data structure and column details
  - The dataset uses structured columns with units where applicable, including:
    - Source_Reference, Animal, Age_Years, Product_Or_Tissue, Radionuclide, Element, Study_Type, Contamination_Route, Source_Of_Radionuclide, Temperature_Degrees_Centigrade, Live_Weight_kg, Length_Of_Study_Days, Number_of_Animals, Sex, Number_Of_Meaurements_To_Determine_Biological_Half_Life.
    - Biological_Half_Life_Single_Days and up to Biological_Half_Life_e_Days (for multiple loss components a–e).
    - Fraction_Released_During_Process_a through Fraction_Released_During_Process_e.
    - Notes, Milk_Yield_Litres_Per_Day, Milk_Yield_SD_Litres_Per_Day, Stage_Of_Lactation_Days, Language_If_Not_English.
  - Many fields are “not information available” or “not applicable,” reflecting variability and reporting differences across sources.
  - Explicitly includes both human-food-chain related data and ancillary data (for modelling context) sourced from the same references.

- Notable caveats and interpretation guidance
  - Differences in the number of loss components reported across studies require interpretation; simple aggregation (means, distributions) is not always appropriate.
  - Some entries may be non-English; language metadata is provided.
  - Data availability varies by animal, product, and radionuclide; not all combinations are equally represented.

- Use and applications
  - Enables development and refinement of radiological protection models that simulate radionuclide transfer through farm animals to human food products.
  - Supports dynamic modelling of radionuclide behaviour (e.g., radiocaesium, iodines, strontium) in different animal products under various conditions.

- References and breadth
  - The dataset cites an extensive set of literature spanning decades and languages, illustrating comprehensive coverage of radionuclide metabolism in farm animals.

- Funding and project context
  - Part of the CONFIDENCE project within the CONCERT European Joint Programme (EJP), funded under the European Union’s Horizon 2020 programme (grant agreement No 662287).