# README for code with the paper: PAG et al., "Fighting force and experience combine to determine contest success in a warlike mammal"

## Overview
- Provides an annotated suite of R code to reproduce analyses from the paper, including imputation, Bayesian analysis, and comparison to maximum likelihood.
- Emphasizes data preparation, quality checks, and exploration of data-driven results.
- Aimed at enabling re-running analyses and understanding data-driven conclusions.

## Data and Data Files
- Pre-imputation data files used by the analyses:
  - pre-imputation_igi_winloss_focalonly_wpregnant
  - pre-imputation_rival_igi_winloss_wpregnant
  - pre-imputation_group_comp_wpregnant
  - pre-imputation_rival_group_comp_wpregnant
  - pre-imputation_rival_group_comp_wpregnant
  - combined_field_capture_weight_data_wpregnancy
- All pre-imputation data are created by an accompanying data generation step.
- Outputs and models used in analyses:
  - mod.names.AICs.combined.dataframe.1 → mod.names.AICs.combined.dataframe.5
  - mod.avg.coef.df.1 → mod.avg.coef.df.5
  - var.imp.df.1 → var.imp.df.5
  - FE.rds
  - ML_model_output
- Documentation for datasets is in data-description.doc.

## Analysis Pipeline
- Imputation_Checking_code: verifies that the imputation process does not bias group weight data.
- Imputation_Analysis_Code_FINAL: performs full imputation and the analysis on imputed datasets.
- Bayesian_Analysis: runs a Bayesian analysis on the same imputed datasets for comparison with the maximum likelihood approach.

## Output Analyses
- IGI_OutputAnalyses summarizes outputs from imputation and analysis steps and compares Bayesian results to ML results.
- Data inputs for this step include:
  - mod.names.AICs.combined.dataframe.1 → mod.names.AICs.combined.dataframe.5
  - mod.avg.coef.df.1 → mod.avg.coef.df.5
  - var.imp.df.1 → var.imp.df.5
  - FE.rds
  - ML_model_output

## Follow-Up Analyses
- IGI_FollowUpAnalyses_FINAL conducts the follow-up analyses described in the main text.
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
  - lifehistory 20210525 (updated life history data for eviction analysis)

## Data Provenance and Revisions
- Files with “REVISION” in their names indicate post-revision changes.
- The data-description.doc provides detailed information about datasets.
- For missing files or bugs, contact PAG at pagreen@ucsb.edu.

## Practical Notes for Data Support
- The workflow is designed to be re-run with annotated code to facilitate data reuse across topics.
- Outputs and models are structured to allow comparison across analytic approaches (Bayesian vs ML) and to support further data exploration and product creation.
- Outputs are intended to be shareable and to promote broader data use, with attention to quality assurance and data provenance.