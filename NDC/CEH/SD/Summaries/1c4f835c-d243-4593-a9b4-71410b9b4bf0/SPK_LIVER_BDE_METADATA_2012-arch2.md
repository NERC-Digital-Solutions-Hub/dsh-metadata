# Bird Data Fields and Explanations

- Purpose: A standardized data schema to capture bird-related findings from post-mortem examinations for environmental health monitoring and policy performance assessment.

## What the dataset captures

- Unique identifier:
  - CEH_BIRD_CODE: Unique identifier assigned to each bird on receipt.
- Biological metadata:
  - SEX: Male or female.
  - AGE_CLASS: Adult or juvenile (juveniles defined as birds hatched in the current or previous calendar year).
- Condition and physical measurements:
  - BODY_CONDITION: Starved or non-starved; starved defined by complete lack of fat deposits or minimal fat around the heart.
  - BOGY_WEIGHT_G: Bird weight at post mortem (grams).
  - LIVER_WT_G: Liver weight (grams).
  - PERCENT_LIPID_IN_LIVER: Percentage of lipid content in the liver.
- Temporal data:
  - MONTH_DIED: Month found deceased (categories: April–Sept or Oct–Mar).
  - YEAR_BIRD_DIED: Year the bird was found deceased.
- Contaminant measurements:
  - BDE47, BDE99, BDE100, BDE138, BDE153, BDE154, BDE183: Concentrations of individual polybrominated diphenyl ether congeners (ng/g lipid weight); not detected (ND) values are substituted with a value below the limit of detection (LoD) using the Hesel method.
  - TOTAL: Total BDEs concentration (ng/g lipid weight).

## Data quality and handling

- ND values for BDE congeners are replaced using the Hesel method to reflect non-detects.
- Units:
  - Weights: grams (g).
  - Liver lipid measures: percent (% for lipids; g for weights).
  - Contaminants: ng/g lipid weight.

## Data processing and outputs

- Data verification, quality assurance, cleaning, and transformation follow established data practices.
- Analyses use standardized methods to categorize environmental health against standards.
- Findings are presented in clear formats (reports, maps, charts).
- Datasets are stored and uploaded to appropriate portals to support access and reuse.

## Practical challenges and opportunities

- Challenge: Increase the value of datasets by integrating with other relevant data rather than using datasets in isolation.
- Challenge: Enable broad access to the underlying data used to produce final outputs, facilitating transparency and secondary analyses.