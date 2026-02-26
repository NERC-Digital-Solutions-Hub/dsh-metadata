# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

## Overview
- Describes datasets used for analyses of intergroup contests among banded mongooses in Mweya, Uganda (2000–2019).
- Includes life-history, morphological, genetic pedigree, and contest-outcome data, plus outputs of the original analyses for result verification.
- Data are designed to support analyses in R via accompanying README documentation.

## Data assets and contents
- Datasets cover:
  - Life-history data for individual mongooses
  - Morphological measurements (e.g., weight, body dimensions)
  - Genetic pedigree information
  - Outcomes of intergroup contests (group-level interactions)
  - Outputs from original analyses for validation
- File-specific examples referenced:
  - combined_field_capture_weight_data_wpregnant (weight, pregnancy status, timing, individual, group, etc.)
  - life_history data (dates, pack, individual, sex, start/end codes, etc.)
  - full pedigree datasets (e.g., 2020 complete pedigree; 2016–older assignments)
  - oestrus, pre-imputation and rival group components related to contest events
  - Lifehistory_20210525 and Lifehistory_20210525-related fields
- Each data entry includes a sampling date (numeric format) tied to the observation.

## Sampling regime and fieldwork
- Data collected near-daily for groups and group members; contest data captured as feasible during sampling.
- Weight and morphological data collected at regular intervals via trapping or resting on scales.
- Blood samples used to establish pedigree data.

## Instruments, data collection methods, and calibration
- Data collection tools:
  - Hand recording, Psion Walkabout digital collectors, and a tablet-based bespoke system
  - Field-based scales, calipers, and other measurement tools
- Pedigree data gathered through blood samples in the field.
- Equipment regularly calibrated; calibration details available at www.socialis.org.
- Documentation available via pagreen@ucsb.edu for calibration-related information.

## Data formats, units, and metadata
- Recorded values have units described in the corresponding col_explanation or are self-explanatory.
- Data tables include standardized column headings (e.g., date, INDIV, PACK, SEX, weight, age, etc.) with descriptive metadata for each column.
- A large portion of the data is organized into multiple dataset files with consistent schema to facilitate joins and analyses.

## Analytical methods and reproducibility
- Analyses are conducted in R; associated code provides methodological details and model checks.
- The datasets are intended to support large-scale data analyses of field-collected observations.
- Outputs of original analyses are included to assist verification and reproducibility.

## Data quality and governance
- Field team comprises six Ugandan researchers with extensive field experience (75+ years combined).
- Quality control measures are implemented within the R code, including model-fit checks and data validation.
- Metadata and column explanations aim to clarify data provenance, variable definitions, and coding schemes.
- Data are designed to support ongoing updates and validation through iterative analyses and user feedback.

## Access, provenance, and contact
- Calibration and supplemental details accessible via www.socialis.org or by contacting pagreen@ucsb.edu.
- The dataset description emphasizes provenance from field collection to laboratory pedigree work and analytical outputs, with supporting documentation accommodated in README and related files.

## Relevance to data-leadership and system perspective
- Illustrates an end-to-end data lifecycle: collection, measurement, calibration, storage, metadata, analysis, validation, and dissemination.
- Demonstrates data discovery across multiple interrelated datasets (field observations, measurements, pedigrees, and contest outcomes) and the need for robust metadata to ensure discoverability and reuse.
- Highlights governance aspects: data quality assurance, documentation, reproducibility of analyses, and collaboration across teams and partners.