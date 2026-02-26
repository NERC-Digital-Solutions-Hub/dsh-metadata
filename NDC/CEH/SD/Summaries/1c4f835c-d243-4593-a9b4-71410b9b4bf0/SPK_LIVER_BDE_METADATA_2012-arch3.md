# Bird Data File: Post-Mortem Measurements and BDE Concentrations

## Overview
- A dataset documenting individual birds with post-mortem measurements and concentrations of polybrominated diphenyl ether (BDE) congeners.
- Intended to support environmental health monitoring, assessment of contaminant exposure, and informing policy decisions through standardized measures and transparent data handling.

## Key variables and their meanings
- CEH_BIRD_CODE: Unique identifier assigned to the bird on receipt.
- SEX: Sex of the bird (Male or female).
- AGE_CLASS: Age classification (Adult or juvenile). Juveniles defined as birds hatched in the current or previous calendar year.
- BODY_CONDITION: Condition at inspection (Starved or non-starved). Starved indicates complete lack of fat deposits or minimal fat around the heart.
- BOGY_WEIGHT_G: Body weight at post-mortem in grams.
- MONTH_DIED: Month the bird was found deceased (categories: April–Sept or Oct–Mar).
- YEAR_BIRD_DIED: Year the bird was found deceased.
- LIVER_WT_G: Weight of the liver in grams.
- PERCENT_LIPID_IN_LIVER: Percentage of lipid in the liver.
- BDE47, BDE99, BDE100, BDE138, BDE153, BDE154, BDE183: Concentrations of individual BDE congeners in ng/g lipid weight.
- TOTAL: Concentrations of total BDEs in ng/g lipid weight.

## Data handling and processing notes
- Not detected (ND) values for BDE congeners are assigned as values below the limit of detection (LoD) using the Hesel method.
- All BDE measurements (except TOTAL) are reported in ng/g lipid weight.
- MONTH_DIED and YEAR_BIRD_DIED provide temporal context for exposure assessment.
- Metadata and documentation accompany the dataset to support data quality and comparability.

## Data quality, governance, and use for monitoring frameworks
- The data dictionary-like structure clearly defines each variable, units, and interpretation to support consistent monitoring across programs.
- Practical use includes tracking environmental contaminant exposure in birds, informing trends over time, and supporting policy evaluations.
- Considerations for monitoring frameworks:
  - Ensure metadata completeness and standardization across datasets to facilitate data sharing and integration.
  - Address data gaps and access barriers that may limit timely analysis.
  - Maintain transparent data governance and provenance, especially for ND imputation methods and lipid-normalized concentrations.