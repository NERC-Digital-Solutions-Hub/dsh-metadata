# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

- Overview
  - Datasets related to analyses of intergroup contests among banded mongooses in Uganda from 2000 to 2019.
  - Includes life-history data for individuals, morphological measurements (size, weight), genetic pedigree data, and contest-outcome data between groups.
  - Also includes outputs of original analyses to support replication and verification.
  - Designed for use with R; a README.doc provides code and details for analyses.

- Data content and structure
  - Core data types:
    - Life-history data (individuals, events, dates)
    - Morphological data (weight, body measurements)
    - Genetic pedigree data (pedigrees, parentage, genotyping outcomes)
    - Contest outcomes data (intergroup competition events, winners, dates, participants)
  - Data are organized into multiple datasets/datasets-like tables, each with its own data dictionary and column definitions.
  - Examples of dataset names present:
    - combined_field_capture_weight_data_wpregnancy
    - final 2020 complete pedigree
    - pre-imputation_group_comp_wpregnant
    - life_history
    - Lifehistory_20210525
  - Column types cover identifiers (INDIV, PACK), demographic attributes (SEX, DOB, age), measurements (weight, head width, head length, body length), event codes (START/END, CODE), dates (DATEN, life_history dates, etc.), and various model/analysis outputs (ML_model_output, mod.avg.coef.df, var.imp.df, etc.).

- Data collection and fieldwork
  - Data collected near-daily for groups and their members; contest data recorded as feasible during sampling.
  - Measurements obtained through trapping and weighing on scales, or during routine handling; some data collected at field sites with portable devices.
  - Pedigree data collected via blood samples in the field.
  - Each data entry includes sampling date (numeric date).

- Instrumentation, calibration, and metadata
  - Field data collection tools include Psion Walkabout digital data collectors and a bespoke tablet-based system.
  - Laboratory/field equipment used for measurements includes field scales, calipers, and related instruments.
  - Equipment calibration performed regularly.
  - Calibration and additional data details available at www.socialis.org or by emailing pagreen@ucsb.edu.
  - Units and data descriptions are documented in the data columns (e.g., weight in grams, head dimensions in cm, age in days).

- Data quality control and reproducibility
  - Data collection executed by a team of six Ugandan researchers with extensive field experience (over 75 total years).
  - Quality control procedures described within the associated R codes, including model-fit checks and data validation steps.
  - The dataset includes outputs from original analyses to facilitate checking and replication of results.

- Analytical methods and reproducibility
  - All analyses are described as based on large-field dataset analyses using R.
  - A README.doc provides detailed analytical steps and code to reproduce results.
  - Data dictionaries and column explanations accompany dataset files, enabling reproducible data preparation and analysis.

- Data governance, sharing, and stewardship considerations
  - Documentation emphasizes data provenance, meticulous metadata, and alignment with data user needs (Data Stewards should ensure:
    - Clear metadata and data dictionaries are maintained and updated.
    - Standardization of formats across datasets and across time.
    - Clear provenance, including collection methods, instruments used, and calibration status.
    - Consistent handling of date formats (numeric dates) and identifiers (INDIV, PACK).
    - Updates to datasets are tracked and shared with accompanying documentation.
  - Access is tied to the dataset’s README and calibration details; contact information is provided for further details.

- Practical use and applicability for Data Stewards
  - Suitable for researchers conducting replication studies or new analyses of banded mongoose contests and life-history dynamics.
  - Supports cross-dataset integration (life-history, morphology, pedigree, and contest outcomes) for comprehensive analyses.
  - Rich metadata and a robust QA/QC framework enhance discoverability, interoperability, and trust in data quality.