# README for code with the paper: PAG et al., "Fighting force and experience combine to determine contest success in a warlike mammal"

- Purpose
  - Provides R-based code to reproduce analyses from the associated paper.
  - Codes are heavily annotated to facilitate re-running analyses.
  - Data descriptions are in data-description.doc.
  - Files changed after revision are labeled with REVISION.
  - If files are missing or bugs found, contact PAG at pagreen@ucsb.edu.

- Code modules and workflow
  - IMPUTATION_ANALYSIS
    - Imputation_Checking_code: verifies that group weight data are not biased by imputation.
    - Imputation_Analysis_Code_FINAL: full imputation and analysis workflow.
    - Bayesian_Analysis: compares Bayesian analysis with the maximum likelihood approach on the same imputed datasets.
    - All codes rely on five pre-imputation data files:
      1) pre-imputation_igi_winloss_focalonly_wpregnant
      2) pre-imputation_rival_igi_winloss_wpregnant
      3) pre-imputation_group_comp_wpregnant
      4) pre-imputation_rival_group_comp_wpregnant
      5) pre-imputation_combined_field_capture_weight_data_wpregnant
  - OUTPUT_ANALYSES
    - IGI_OutputAnalyses: summarizes outputs from the imputation and analysis steps; compares Bayesian vs ML outputs.
    - Uses data files that map between mod.names, AICs, coefficients, and variable importance, plus final model outputs:
      - mod.names.AICs.combined.dataframe.1 → ... → mod.names.AICs.combined.dataframe.5
      - mod.avg.coef.df.1 → ... → mod.avg.coef.df.5
      - var.imp.df.1 → ... → var.imp.df.5
      - FE.rds
      - ML_model_output
  - FOLLOW_UP_ANALYSES
    - IGI_FollowUpAnalyses_FINAL: conducts all follow-up analyses described in the main text.
    - Requires multiple datasets, including:
      - combined_igi_list_node1.2_reps1_2000.rds
      - focal_group_comp_list_node1.2_reps1_2000.rds
      - rival_group_comp_list_node1.2_reps1_2000.rds
      - life_history
      - captures
      - oestrus
      - full parentage assignments to 2016
      - final 2020 complete pedigree 29-06-20
      - Evictees
      - lifehistory 20210525 (updated eviction analysis)

- Data inputs and dependencies
  - Data generation code creates the required inputs for the analyses.
  - Pre-imputation data cover IGI win/loss, rival performance, group competition, and pregnancy context.
  - A separate dataset, combined_field_capture_weight_data_wpregnant, provides weighted field capture information.
  - Follow-up analyses integrate life history, capture data, oestrus, and pedigree/ejection-related datasets.

- Outputs and results
  - Outputs include comparisons between Bayesian and maximum likelihood results, coefficient estimates, and variable importance rankings.
  - Detailed follow-up results link to life history, eviction-related data, and complete pedigree information through 2020.

- Revisions, housekeeping, and contact
  - Filenames marked REVISION indicate updated files.
  - If issues arise or files are missing, please contact pagreen@ucsb.edu.