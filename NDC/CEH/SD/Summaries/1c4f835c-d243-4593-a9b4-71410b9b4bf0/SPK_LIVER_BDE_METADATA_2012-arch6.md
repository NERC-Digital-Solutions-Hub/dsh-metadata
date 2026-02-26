# CEH_BIRD_CODE, EXPLANATION = Unique identifier assigned to bird on receipt.

- Purpose of the data: A dataset containing post-mortem biological measurements and chemical analyses for birds, enabling analysis of physical condition and contaminant levels (BDEs) alongside basic metadata.

- Key identifiers and basic fields:
  - CEH_BIRD_CODE: Unique identifier assigned to each bird on receipt.
  - SEX: Male or female.
  - AGE_CLASS: Adult or juvenile (juveniles defined as birds hatched in the current or previous calendar year).
  - MONTH_DIED: Month found deceased, encoded as April-Sept or Oct-Mar.
  - YEAR_BIRD_DIED: Year the bird was found deceased.

- Biological measurements:
  - BODY_CONDITION: Starved or non-starved, based on post-mortem assessment.
  - BOGY_WEIGHT_G: Weight of the bird at post-mortem (grams).
  - LIVER_WT_G: Weight of the liver (grams).
  - PERCENT_LIPID_IN_LIVER: Percent lipid content in the liver.

- Contaminant analyses (all concentrations in ng/g lipid weight):
  - BDE47, BDE99, BDE100, BDE138, BDE153, BDE154, BDE183: Concentrations of individual BDE congeners.
  - TOTAL: Total BDE concentration.

- Data quality and handling notes:
  - Not detected (ND) values are assigned a value below the limit of detection (LoD) using the Hesel method.
  - UNITS are specified for each field; several fields have N/A where not applicable (e.g., CEH_BIRD_CODE, YEAR_BIRD_DIED).
  - Data may come in a patchy or varied format and may require harmonization when combining datasets from different systems.

- Practical data use and preparation guidance for data support:
  - Build self-serve dashboards or pivotable reports to explore relationships between body condition, liver lipid content, and BDE concentrations across sex, age class, and time (month/year).
  - Clean and harmonize formats for MONTH_DIED and YEAR_BIRD_DIED to enable temporal analyses.
  - Handle ND values consistently using the documented LoD method (Hesel) to ensure comparability across samples.
  - Consider unit consistency and potential data gaps when integrating with other datasets (e.g., combining with external environmental or species data).

- Potential analysis angles:
  - Compare liver lipid percentage and starvation status with total BDE burden.
  - Assess whether BDE concentrations vary by sex or age class.
  - Examine seasonal patterns by month of death and year, and relate to exposure or mortality factors.