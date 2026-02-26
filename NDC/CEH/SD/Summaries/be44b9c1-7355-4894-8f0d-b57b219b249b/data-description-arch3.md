# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

- Purpose and scope
  - Datasets describing analyses on the outcomes of banded mongoose contests (intergroup interactions) in Uganda from 2000 to 2019.
  - Includes data to be used with accompanying R code and to enable replication of original analyses; outputs of analyses are included to aid verification.

- Content of the datasets
  - Life-history data for individual mongooses.
  - Morphological data (size, weight) and related measurements.
  - Genetic pedigree data.
  - Data on contest outcomes between groups (packs).
  - Additional data outputs from the original analyses to assist replication and checking results.

- Experimental design and sampling regime
  - Data collected near-daily for focal groups and their members.
  - Contest data collected as feasible during sampling periods.
  - Weight and morphological measurements obtained at regular intervals via trapping or trained weighing.

- Fieldwork and laboratory instrumentation
  - Data captured with manual methods, Psion Walkabout devices, or a tablet-based data collection system.
  - Field instruments include scales, calipers, and related equipment; pedigree data obtained from field-collected blood samples.

- Calibration, data quality, and documentation
  - Equipment regularly calibrated; calibration details available at www.socialis.org or by contacting pagreen@ucsb.edu.
  - Data entries include dates (numeric format) and are accompanied by comprehensive metadata and field explanations.

- Nature, units, and metadata of recorded values
  - Units noted in the data or described in the col_explanation/col_heading metadata.
  - Rich metadata embedded in the dataset, with explicit column explanations and data dictionaries.

- Analytical methods and reproducibility
  - Associated R code documents the analytical methods used on the large field-collected dataset.
  - Analyses rely on comprehensive, high-volume data assembled from field observations.

- Data governance, quality control
  - A team of six Ugandan researchers provides data collection with substantial field experience.
  - Quality control measures described in the R code, including model-fit checks and data validation steps.

- Data structure and representative files
  - Multiple files with descriptive names serving various aspects (examples):
    - combined_field_capture_weight_data_wpregnancy
    - final 2020 complete pedigree
    - Lifehistory_20210525
    - pre-imputation_group_comp_wpregnant
    - pre-imputation_rival_group_comp_wpregnant
    - oestrus
  - Each file comprises multiple related columns (e.g., date, indiv, pack, sex, weight, various morphometrics, event identifiers, pedigree links, life-history codes, and metadata).
  - The dataset includes columns for data provenance, coding of events (e.g., eviction, contest), and numeric dates, with descriptive headings and explanations.

- Access, reuse, and contact
  - Calibration and contextual details available via www.socialis.org or by emailing pagreen@ucsb.edu.
  - Documentation and data dictionary accompany the datasets to support reuse and replication.

- Relevance for monitoring frameworks
  - Demonstrates thorough data description, metadata clarity, and data provenance—key for monitoring frameworks.
  - Provides a model of handling long-term ecological data: daily/near-daily collection, standardized measurements, pedigree linkage, data transformation, and transparent reporting of metadata.
  - Highlights practical governance considerations: data sharing barriers, metadata completeness, transformation requirements, and the importance of clear data provenance to enable policy scrutiny and future decision-making.