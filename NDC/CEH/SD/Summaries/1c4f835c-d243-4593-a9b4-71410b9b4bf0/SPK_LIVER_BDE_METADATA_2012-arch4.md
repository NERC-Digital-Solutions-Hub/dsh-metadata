# Bird Data Variables and Descriptions for Post-Mortem Analysis

## Overview
- A data dictionary for post-mortem bird analysis, documenting identifiers, demographics, physical state, temporal context, and chemical concentrations (BDEs) with explicit explanations, units, and notes on data handling (e.g., ND values below the limit of detection).

## Data Model and Key Fields
- CEH_BIRD_CODE: Unique identifier assigned to the bird on receipt.
- SEX: Sex of the bird (Male or Female).
- AGE_CLASS: Age classification (Adult or Juvenile; juveniles defined as birds hatched in the current or previous calendar year).
- BODY_CONDITION: Condition of the bird (Starved or Non-starved; Starved defined as severe fat depletion at post-mortem).
- BOGY_WEIGHT_G: Bird weight at post mortem (grams).
- MONTH_DIED: Month the bird was found deceased (April–Sept or Oct–Mar).
- YEAR_BIRD_DIED: Year the bird was found deceased.
- LIVER_WT_G: Weight of the liver (grams).
- PERCENT_LIPID_IN_LIVER: Percent lipid found in the liver.
- BDE47, BDE99, BDE100, BDE138, BDE153, BDE154, BDE183: Concentrations of individual BDE congeners (ng/g lipid weight); Not detected values are assigned below the LoD using the Hesel method.
- TOTAL: Concentrations of total BDEs (ng/g lipid weight).

## Data Quality, Processing, and Metadata
- ND (Not Detected) values are imputed as values below the limit of detection (LoD) following the Hesel method.
- Units are specified for each field (e.g., g, ng/g lipid weight, %).
- clear EXPLANATION, UNITS, and NOTES accompany every field to support data interpretation and reuse.

## Data Governance, Standards, and Provenance
- Naming convention uses a consistent prefix (CEH_) for the identifier, aiding discoverability and cross-dataset integration.
- Metadata-focused design supports data provenance, traceability of measurements, and methodological consistency (LoD handling via Hesel method).

## Use Cases and Stakeholders
- Health and physiological assessment: relate body condition, weight, and liver lipid content to overall bird health.
- Environmental exposure assessment: analyze BDE concentrations and total BDE burden.
- Temporal and seasonal analyses: leverage MONTH_DIED and YEAR_BIRD_DIED for trend analysis.
- Cross-partner collaboration: standardized fields and notes facilitate data sharing across networks of researchers.

## Challenges and Gaps
- ND handling depends on the Hesel method; differences in LoD reporting across datasets could affect comparability.
- Juvenile definitions rely on birth timing, which may require cross-referencing with other datasets for precise age validation.
- Potential variability in laboratory methods across sites if data are pooled from multiple sources.

## Recommendations for Data Leaders
- Ensure complete documentation of LoD determination method (Hesel) and provenance to maximize cross-dataset compatibility.
- Maintain strict metadata discipline (explanations, units, notes) to support discoverability and reuse.
- Standardize data collection and reporting protocols across partners to minimize method-driven batch effects.
- Implement data quality checks to detect inconsistencies in units, age classifications, and ND handling.
- Facilitate data integration by aligning with broader data dictionaries and providing clear mappings to similar variables in other datasets.