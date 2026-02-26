# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

- Provides datasets for analyses on intergroup contests among banded mongooses in Mweya Peninsula, Uganda (2000–2019)
- Includes life-history data on individuals, morphological measurements (size, weight), genetic pedigree data, and data on contest outcomes between groups
- Also includes outputs from original analyses to facilitate validation of results

## Scope and contents

- Core data types
  - Life-history data: individual-level timing and events (births, deaths, migrations, group changes)
  - Morphology: size, weight (gram-scale), body measurements
  - Genetic pedigree data: parentage, dams and sires, pedigree reliability and related probabilities
  - Contest outcomes: records of intergroup contests, including participants, winners, and contest logistics
- Additional data for replication and verification
  - Outputs of original analyses for cross-checking results
- Time and place
  - Data collected from 2000 to 2019 in the Mweya Peninsula, Uganda

## Data collection and field methods

- Collection regime
  - Near-daily observations of groups and group members
  - Contests recorded as feasible during data collection
  - Weight and morphological data collected at regular intervals via trapping or trained weighing on scales
- Data capture tools
  - Psion Walkabout digital data collectors
  - Bespoke tablet-based data collection system
- Laboratory and field equipment
  - Field-based scales, calipers, and related equipment for measurements
  - Blood samples collected for pedigree data
- Dates and timing
  - Each entry includes sampling date (numeric format)

## Calibration, units, and documentation

- Calibration
  - Equipment regularly calibrated
  - Detailed calibration information available via www.socialis.org or pagreen@ucsb.edu
- Units and descriptions
  - Recorded values have self-explanatory units; column explanations provided in accompanying metadata and documentation
- Documentation and reproducibility
  - Analytical methods are described, with R code used for analyses
  - README.doc describes the R code and analysis workflow

## Data structure and key datasets

- Primary datasets described (with many accompanying metadata fields)
  - combined_field_capture_weight_data_wpregnancy
  - final 2020 complete pedigree
  - Lifehistory_20210525
  - pre-imputation_group_comp_wpregnant
  - pre-imputation_rival_group_comp_wpregnant
  - pre-imputation_igi_winloss_focalonly_wpregnant
  - oestrus
  - Lifehistory_20210525 and related life-history files
  - Various pre-imputation and post-imputation datasets related to group competition, winner determination, and guardings
- Common fields across datasets (illustrative examples)
  - DATEN / Date in numeric or day-month-year format
  - PACK / group (pack) ID
  - INDIV / individual ID
  - SEX / sex
  - WEIGHT / weight (grams)
  - AGE / age (days) on weighing date
  - dob / date of birth
  - pregnancy status (pregnant)
  - weight type (field or lab)
  - life-history codes (START/END, CODE, EXACT)
  - pedigree fields (dam, sire, assignment methods, probabilities)
  - pedigree quality indicators (MB_dam_prob, MB_sire_prob, assignmentprobs, etc.)
  - discussion-ready outputs from statistical models (mod.avg.coef.df, AICs, var.imp.df, etc.)
- Purpose of the variety of files
  - Supports longitudinal analyses of individuals and groups
  - Allows integration of field observations with genetic relationships
  - Enables replication and validation of original analyses through provided outputs

## Quality assurance and data governance

- Team and expertise
  - Data collection conducted by a team of six Ugandan researchers with extensive field experience (75+ years combined)
- Quality control
  - Quality checks and model-fit validations described within the associated R code
- Data provenance and usability
  - Datasets and metadata designed to be discoverable and usable; associated documentation and scripts provided
  - Data are designed to be used with the accompanying README.doc and R code for analyses

## Intended use and access

- Primary use
  - To enable analysis of life-history, morphology, pedigree structure, and intergroup contest outcomes
  - To allow replication and validation of original analyses and modeling approaches
- Access to metadata and further details
  - Calibration steps and dataset-specific details are documented
  - Original analysis code and documentation are available through the stated channels
  - Contact pagreen@ucsb.edu or visit www.socialis.org for additional calibration and metadata details
- Reproducibility and data sharing
  - Datasets include outputs from original analyses to facilitate checking results
  - Documentation and multiple data files support rigorous reproducibility and cross-validation of findings