# README for code with the paper:
PAG et al., "Fighting force and experience combine to determine contest success in a warlike mammal"

## Overview
- Provides annotated R code to reproduce analyses from the PAG et al. paper.
- Codes are organized into dedicated scripts for imputation, analysis, output summarization, and follow-up analyses.
- Most files are R scripts; heavily annotated to facilitate re-running analyses.
- Data description is documented separately in data-description.doc.

## Data and datasets
- Data description: dataset information available in data-description.doc.
- Core data files used by all code:
  - pre-imputation_igi_winloss_focalonly_wpregnant
  - pre-imputation_rival_igi_winloss_wpregnant
  - pre-imputation_group_comp_wpregnant
  - pre-imputation_rival_group_comp_wpregnant
  - combined_field_capture_weight_data_wpregnancy
- These data files are produced by the data generation code described in the project.
- Follow-up and auxiliary data referenced by the analyses include:
  - life_history
  - captures
  - oestrus
  - full parentage assignments to 2016
  - final 2020 complete pedigree 29-06-20
  - Evictees
  - lifehistory 20210525 (updated for eviction analysis)

## Code structure and workflows
- IMPUTATION_ANALYSIS
  - Imputation_Checking_code: validates that imputation does not bias group weight data.
  - Imputation_Analysis_Code_FINAL: complete imputation and analysis pipeline.
  - Bayesian_Analysis: Bayesian analysis on the same imputed datasets for comparison with maximum likelihood results.
- OUTPUT_ANALYSIS
  - IGI_OutputAnalyses: summarizes outputs from imputation and analysis; compares Bayesian and ML results.
  - Uses data files transformed/structured as:
    - mod.names.AICs.combined.dataframe.1 to .5
    - mod.avg.coef.df.1 to .5
    - var.imp.df.1 to .5
    - FE.rds
    - ML_model_output
- FOLLOW_UP_ANALYSES
  - IGI_FollowUpAnalyses_FINAL: conducts all follow-up analyses described in the main text.
  - Data inputs include:
    - combined_igi_list_node1.2_reps1_2000.rds
    - focal_group_comp_list_node1.2_reps1_2000.rds
    - rival_group_comp_list_node1.2_reps1_2000.rds
    - life_history
    - captures
    - oestrus
    - full parentage assignments to 2016
    - final 2020 complete pedigree 29-06-20
    - Evictees
    - lifehistory 20210525 (updated for eviction analysis)

## Data provenance, metadata, and reproducibility
- All code is designed to be reproducible and rerunnable, with clear data dependencies.
- Data lineage is documented via explicit input file names and the data description document.
- File revisions are tracked in filenames with "REVISION" to indicate updates post-review.
- Heavily annotated code aids understanding of each analysis step and data transformation.

## Access, contact, and versioning
- For missing files or bug reports, contact PAG at pagreen@ucsb.edu.
- Data and code are organized into clearly named directories, with separate scripts for imputation, analysis, outputs, and follow-up analyses.
- The project relies on multiple interdependent datasets and outputs; maintainers should ensure all referenced inputs are present for full reproducibility.

## Data governance considerations for Data Stewards
- Ensure metadata completeness by referencing data-description.doc for each dataset.
- Maintain version control on data and code by preserving revision-tagged filenames and documenting changes.
- Monitor data privacy and integrity when handling large, multi-source datasets (as indicated by pre-imputation and post-imputation data, plus pedigree and eviction-related data).
- Establish provenance trails across the full analysis pipeline from data generation to final outputs and follow-up analyses.
- Provide clear access points for datasets and outputs to enable discovery and reuse by others.