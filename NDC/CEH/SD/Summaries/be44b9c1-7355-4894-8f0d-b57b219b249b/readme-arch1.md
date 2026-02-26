# Fighting force and experience combine to determine contest success in a warlike mammal

## Overview
- README for code accompanying the PAG et al. paper; most codes are .R files with extensive annotations to aid re-running analyses.
- Data descriptions are in data-description.doc; revision changes are labeled with "REVISION" in filenames.
- If files are missing or bugs exist, contact PAG at pagreen@ucsb.edu.

## Code modules and purpose
- Imputation analysis
  - Imputation_Checking_code: verifies that the imputation process does not bias group weight data.
  - Imputation_Analysis_Code_FINAL: performs the full imputation and analysis.
  - Bayesian_Analysis: runs a Bayesian analysis on the imputed datasets for comparison with the maximum likelihood approach.
- All imputation and analysis use the following data files (pre-imputation stage):
  - pre-imputation_igi_winloss_focalonly_wpregnant
  - pre-imputation_rival_igi_winloss_wpregnant
  - pre-imputation_group_comp_wpregnant
  - pre-imputation_rival_group_comp_wpregnant
  - combined_field_capture_weight_data_wpregnant

## Data files and generation
- These pre-imputation data files are created by the data generation code described in the README.

## OUTPUT_ANALYSIS
- IGI_OutputAnalyses: summarizes the imputation and analysis outputs and compares Bayesian analysis to maximum likelihood results.
- Uses the following data files:
  - mod.names.AICs.combined.dataframe.1 through mod.names.AICs.combined.dataframe.5
  - mod.avg.coef.df.1 through mod.avg.coef.df.5
  - var.imp.df.1 through var.imp.df.5
  - FE.rds
  - ML_model_output

## FOLLOW_UP_ANALYSES
- IGI_FollowUpAnalyses_FINAL: conducts all follow-up analyses detailed in the main text.
- Uses the following data files:
  - combined_igi_list_node1.2_reps1_2000.rds
  - focal_group_comp_list_node1.2_reps1_2000.rds
  - rival_group_comp_list_node1.2_reps1_2000.rds
  - life_history
  - captures
  - oestrus
  - full parentage assignments to 2016
  - final 2020 complete pedigree 29-06-20
  - Evictees
  - lifehistory 20210525 (updated for eviction analysis; closely related to life_history)

## Data provenance, revisions, and contact
- Data files are created by an accompanying data generation pipeline; revisioned filenames indicate updates.
- For missing files or bugs, contact pagreen@ucsb.edu.