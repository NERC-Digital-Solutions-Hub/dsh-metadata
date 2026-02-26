# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

## Overview
- A collection of datasets related to analyses of intergroup contests among banded mongooses in Uganda from 2000 to 2019.
- Datasets are intended for use with R code described in the README.doc file.
- Includes raw life-history, morphological (size, weight), genetic pedigree, and contest-outcome data, plus outputs from original analyses to aid validation.

## Data contents and scope
- Life-history data for individual mongooses.
- Morphological measurements (e.g., size, weight).
- Genetic pedigree data.
- Data on outcomes of contests between groups (intergroup interactions).
- Outputs of original analyses to help users check results.
- Datasets and fields are structured to support extensive analyses of life history, social structure, and contest dynamics.

## Sampling design and field collection
- Most data are collected near-daily on groups and their members.
- Contest-related data are collected as feasible during data sampling.
- Weight and morphological measurements are taken at regular intervals via trapping or weighing trained individuals.
- Each data entry includes a sampling date in numeric format.

## Data collection methods and instrumentation
- Data collected by hand, on Psion Walkabout digital data collectors, or via a bespoke tablet-based data collection system.
- Field instrumentation includes scales, calipers, and other measurement equipment.
- Pedigree data are derived from blood samples collected in the field.

## Calibration, quality control, and documentation
- Equipment is regularly calibrated.
- Quality control is conducted by a team of six Ugandan researchers with over 75 years of combined field experience.
- Quality control details are documented within the associated R codes, including checks of model fit.
- Calibration and further details are available via www.socialis.org or pagreen@ucsb.edu.

## Data formats, units, and field definitions
- Recorded values are self-explanatory or explained in the col_explanation column of each dataset.
- Dates are stored in numeric formats (with some datasets using day-month-year formats).
- Units are typically:
  - Weight: grams
  - Morphometrics: centimeters
  - Age: days (on the weighing date)
- Example dataset structure (highlights; not exhaustive):
  - combined_field_capture_weight_data_wpregnancy: date, individual ID, pack ID, sex, weight (grams), pregnant, type (field or lab), dob, age, etc.
  - captures: sex, weight, head_width, head_length, body_length, event IDs, dates, packs, individuals, etc.
  - Pedigree data files: final 2020 complete pedigree with dam/sire IDs, assignment methods, probabilities, and related metadata.
  - Life_history datasets: life_history variables including date, pack, individual, sex, start/end codes, exact observations, and related codes.
  - Various pre-imputation and imputation-related datasets (e.g., pre-imputation_group_comp_wpregnant, pre-imputation_rival_group_comp_wpregnant, igi_winloss_focalonly_wpregnant, etc.) containing contest-level and group-level fields used in pedigree and assignment analyses.
  - Lifehistory_20210525 and Lifehistory timelines with standardized fields for life-history and observation codes.
- A wide range of column headings exists across datasets, including date fields, pack/indiv IDs, sex, age, weight, pregnancy status, various measurements (head width/length, body length), event and contest identifiers, and pedigree-related fields.

## Analytical methods and reproducibility
- The datasets are accompanied by R code that details the analytical methods used.
- Analyses are based on large field-collected datasets.
- Outputs from original analyses are included to facilitate verification and reproducibility.

## Availability, usage, and contact
- Documentation and instructions for use are provided in README.doc.
- Calibration and data-support contacts:
  - www.socialis.org
  - pagreen@ucsb.edu

## Key considerations for data support
- The collection integrates multiple data types (biological, behavioral, genetic) across a long time span (2000–2019, plus pedigrees up to 2020).
- Data come from multiple collection platforms (manual, Psion, tablet), necessitating careful data integration and standardization.
- Quality control is a central component, with formal checks embedded in the accompanying R code.
- The dataset structure supports analyses of intergroup contests, social dynamics, life-history strategies, and pedigree-based investigations.