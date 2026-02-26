# Data description for Intergroup contests in banded mongooses (Mungos mungo) on the Mweya peninsula, Uganda, 2000-2019

- Overview
  - Describes datasets relevant to analyses on intergroup contests among banded mongooses in Uganda (2000–2019).
  - Datasets cover life-history data, morphological measurements (size, weight), genetic pedigree data, and contest-outcome data between groups.
  - Includes outputs of original analyses to aid replication and validation, designed to be used with R code described in the README.doc.

- Data scope and components
  - Near-daily data collection on mongoose groups and individuals; contest data collected as feasible during sampling.
  - Weight and morphological data collected at regular intervals via trapping or weighing on trained scales.
  - Pedigree data derived from blood samples; comprehensive life-history and demographic details.
  - Outputs of analyses included for checking results.

- Data collection, instrumentation, and fieldwork
  - Collected by hand, Psion Walkabout devices, or a bespoke tablet-based data collection system.
  - Laboratory-like field instruments include scales, calipers, and other measurement tools.
  - Pedigree data gathered from field blood samples.
  - Sampling date recorded for each entry (numeric date format).

- Calibration, quality control, and standards
  - Equipment routinely calibrated; calibration and related details available via www.socialis.org or by contacting pagreen@ucsb.edu.
  - Quality control performed by a six-person Ugandan research team with extensive field experience.
  - Data analysis quality checks described within the associated R code (model fit checks, etc.).

- Data structure and variable coverage
  - Multiple data tables with extensive field schemas, including:
    - combined_field_capture_weight_data_wpregnancy: captures of weights with pregnancy status and related fields (date, individual ID, group/pack, sex, weight in grams, age, etc.).
    - captures: housing fields such as sex, weight, head width, head length, body length, event IDs, dates, pack and individual IDs.
    - pedigree and genetic data: final 2020 complete pedigree and related assignments, including dam/sire IDs, assignment methods, probabilities, and genotyping status.
    - life_history: longitudinal life-history records with pack and individual IDs, sex, start/end codes, life-history codes, exact observation flag.
    - ML_model_output and mod.* / var.* / mod.names.* / var.imp.* datasets: results and metadata from statistical analyses, permutations, model coefficients, AICs, variable importances, and model listings across multiple runs.
    - oestrus, pre-imputation_group_comp_wpregnant, pre-imputation_rival_group_comp_wpregnant, pre-imputation_igi_winloss_focalonly_wpregnant, etc.: specialized pre-imputation and contest-related variables covering events, dates, focal/rival groups, winners, weights, guard data, and various summary statistics.
  - Variables span identifiers (INDIV, PACK), event dates (DATEN), numeric dates, sex, age in days, weight (grams), anthropometrics (head width/length, body length), pregnancy status, birth dates, adult status, and numerous pre-imputation and post-imputation fields related to group contests and social interactions.
  - Units are either self-explanatory or documented in the col_explanation fields within the datasets.

- Analytical methods and replication
  - Analyses described as based on large field-collected datasets; R code accompanies the data for replication.
  - Outputs include model estimates, permutation results, AICs, and other statistics typical of ecological/behavioral analyses.

- Access, support, and contact
  - Calibration and methodological details available via www.socialis.org or by emailing pagreen@ucsb.edu.
  - Readme/README.doc provides details for using the R code and reproducing analyses.

- Relevance for GIS-focused work
  - Although primarily a behavioral ecology dataset, the data are organized around spatially defined groups (packs) and individual animals with temporal (date-based) records, suitable for GIS-style mapping of group ranges, intergroup interactions, and spatiotemporal analyses when location data are incorporated.