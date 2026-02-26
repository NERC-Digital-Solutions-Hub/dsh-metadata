# Experimental design/collection method: Life history data

- Purpose and scope
  - Document the experimental design, collection methods, and data types for studying how drought stress and landscape origin affect butterfly life history, reproduction, and morphology.
  - Provide data in a way suitable for subsequent analysis, interpretation, and potential policy-relevant monitoring.

- Experimental setup and population sources
  - Four outbred laboratory stock populations from Belgium, representing two landscape types: woodland (Lauzelle, St. Hubert) and agricultural (Lillois, Hoegaarden).
  - Larvae were randomly selected (three per plant) and reared to adulthood on potted host plants of Parietaria trivialis (P. trivialis) under control or drought-stressed conditions, in climate-controlled room, ensuring common garden conditions.
  - Equal representation of each laboratory source population in control and drought-stress treatments.
  - Total larvae assigned: 178 to control, 390 to drought-stress.

- Measured life history and outcomes
  - Development and survival
    - Date of eclosion; total development time (egg to adult).
    - Mean egg-to-adult survival by population.
  - Adult metrics at eclosion
    - Mass (mg) and sex of each adult.
  - Female reproductive output (oviposition phase)
    - 100 females (50 woodland-origin, 50 agricultural-origin) placed individually in cages with host plant, male, and nectar source.
    - Outcomes per female: total eggs laid over life, mean egg size, hatch proportion, female longevity.
  - Wing morphology (post-mortem)
    - Removal and digital imaging of fore- and hindwings; measurements include forewing and hindwing surface areas, wing length, melanization, and derived traits like wing loading and mean forewing melanization.

- Data storage and dataset structure
  - Stored as CSV spreadsheets with three datasets:
    - Life_history_data.csv
    - Female_reproductive_output_data.csv
    - Wing_data.csv
  - Each dataset includes descriptive headers (described below) and unique identifiers for individuals.
  - Missing data are indicated by empty cells.

- Data headers and key variables
  - Life_history_data.csv
    - Population, Description; Landscape, Treatment; ID; Adult_mass; Total_development_time; Square_root_Total_devtime; sex
  - Female_reproductive_output_data.csv
    - Population, Description; Landscape, Description; Treatment, Description; ID; Adult_mass; Mean_egg_size; Longevity; Number_days_until_1st_egg_laid; Fecundity; Arcsine_square_root_%_Eggs_hatched; %Eggs_hatched
  - Wing_data.csv
    - Population, Description; Landscape, Description; Treatment, Description; ID; Adult_mass; Total_development_time; sex; Wing_loading; Mean_forewing_Melanin; Mean_FW_aspect_ratio; Total_Wing_area
  - Notes
    - Units include: Adult_mass (mg); Total_development_time (days); Mean_egg_size (mm^2); Wing_loading (mg/mm^2); Total_Wing_area (mm^2).
    - Empty cells indicate missing data (e.g., due to death of the butterfly).

- Data quality, accessibility, and governance implications
  - Metadata and clarity
    - The dataset provides explicit header descriptions and unit definitions to support interpretation and reuse.
  - Data gaps and barriers
    - Potential data gaps (incomplete records, missing metadata) and the need for careful data cleaning and standardization before reuse.
  - Data sharing and transparency
    - Emphasizes the importance of sharing underlying data and documentation to enhance transparency, though sharing can be a barrier in some contexts.
  - Data transformation and compatibility
    - Some variables may require transformation (e.g., square roots, derived metrics) to meet analysis needs.
  - Timeliness and governance
    - The dataset demonstrates the importance of keeping data well-documented and governed (descriptions of headers, IDs, units) to facilitate future monitoring and policy evaluation.

- Relevance for monitoring and policy evaluation
  - Provides a multi-faceted data foundation (life history, reproduction, and morphology) to assess environmental stressors (drought) and landscape influences on an at-risk or indicator species.
  - Demonstrates a structured approach to data collection, metadata documentation, and data storage that supports reproducibility and transparent monitoring in environmental health policies.
  - Highlights practical considerations for monitoring authors, including data accessibility, dataset organization, and explicit data definitions to reduce ambiguity for end users.