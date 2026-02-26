# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Overview
- A dataset documenting survival and heights of trees planted for forest restoration in South and Southeast Asia, along with analytical code used in Banin, Raine et al. (2023).
- Collated from 176 sites where disturbance or clearance occurred and trees were planted and monitored over time (up to May 2021).
- Analyses model height growth, extract annual size-standardised growth rates (ASGR), and test effects of biophysical, climatic conditions and planting regimes on survival and growth.
- Created to represent current knowledge on forest restoration outcomes in the region; suitable for analyzing mortality and growth dynamics across varied contexts.

## Contents and file structure
- df_study_details.csv: Details of studies and sites for height and/or survival datasets.
- df_survival_Nov2022.csv: Survival data for planted trees.
- df_height_Nov2022.csv: Height data from multiple censuses.
- script_SynthesisAnalysis_MortalityModels.R: R code for mortality analysis.
- height_nlm_functions.R: Functions for fitting linear, exponential, and Gompertz models.
- height_ASGR_nlms.R: Code for fitting height models, model selection, and calculating ASGR.
- script_SynthesisAnalysis_ASGR_MEMs.R: R code for ASGR statistical analysis.
- supporting_info_survival_height.docx: Data collection/processing/analysis details.
- Adaptation and processing notes: Datasets prepared per Banin, Raine et al. (2023) and supplementary materials.

## Data sources and scope
- Data collated from published studies, grey literature, and data provided by co-authors.
- Fields cover field site location, forest type, disturbance history, restoration measures, planting regimes, species, and growth/survival metrics.
- Forest types: TF (tropical forest on mineral soil) and TPSF (tropical peat swamp forest).
- Disturbance categories include logged, agriculture, plantation, fire, mining, and drained.
- Restoration measures captured as six binary indicators (0/1) for activities such as competition removal, shading, soil preparation, water regulation, fertilisation, and protection.

## Variables and coding (key fields)
- Study, Country, Province, Lat_dec, lon_dec: site and location identifiers.
- Disturbance, Forest_condition, Restorations measures: context of restoration activity.
- Plot_id, Treatment, Number_planted, Number_monitored, Duration_months: planting and monitoring details.
- Species_full, Genus, Species, Family: taxonomic details of planted seedlings.
- W_meanWD, W_sdWD, W_levelWD, W_nInd: wood density metrics.
- Site_sp: site-species combination identifier.
- Survey fields: Age_0, Height_0, Height_0_v2 for planting height; Height_cm_v2 for height at later censuses; Height measurements across censuses.
- Survival fields: Survival_per (percentage survival), Number_alive, Number_dead.
- Derived metrics and outputs (from AGR model outputs):
  - Model_AIC: best model (lm, gomp, exp).
  - Ref_height: reference height in cm (100, 200, or 300).
  - SGR: instantaneous size-standardised growth rate at reference height.
  - AGR: Annual Growth Rate when reference height is reached.
  - AGRvar: variance of AGR.
  - Number_census, Duration_months, etc., for temporal context.

## Data processing and analysis workflow
- Processed datasets are produced by running:
  - height_ASGR_nlms.R (fits height models, selects model, and computes ASGR).
  - height_nlm_functions.R (supports height model fitting).
  - script_SynthesisAnalysis_ASGR_MEMs.R (statistical analysis of height growth measures).
- Mortality analyses are conducted with script_SynthesisAnalysis_MortalityModels.R.
- Climate covariates from WorldClim (2.5 arc-minute resolution) are required for mortality and ASGR analyses:
  - vals_temp (annual mean temperature, BIO1)
  - vals_maxTwm (max temperature of warmest month, BIO5)
  - vals_minTcm (min temperature of coldest month, BIO6)
  - vals_precip (annual precipitation, BIO12)
  - vals_pwq (precipitation of wettest quarter, BIO16)
  - vals_pdq (precipitation of driest quarter, BIO17)
  - vals_elev (elevation)
- WorldClim data licensing restricts direct integration within this dataset; thus climate data must be downloaded separately for site locations.
- Wood density data supplied via BIOMASS package (Zanne et al. 2009) in R.

## How to use the data (analytical workflow)
- Use df_height_Nov2022.csv and df_survival_Nov2022.csv for empirical analyses of height growth and survival.
- Run height_ASGR_nlms.R (with height_nlm_functions.R) to generate processed height datasets and ASGR estimates.
- Use script_SynthesisAnalysis_ASGR_MEMs.R to perform statistical analyses on ASGR and growth metrics, incorporating biophysical and climatic covariates (where licensed data are used separately).
- Use script_SynthesisAnalysis_MortalityModels.R to model mortality as a function of predictors (forest type, disturbance, restoration measures, Site-specific factors, etc.) with WorldClim covariates.
- Ensure proper handling of licensing constraints by separating WorldClim data acquisition from this dataset.
- Reference and reproduce Banin, Raine et al. (2023) to align analyses with published methods.

## Field descriptions and content notes
- df_study_details.csv: includes Forest type (TF or TPSF), Unique Identifier Code (UIC), and study references.
- df_survival_Nov2022.csv and df_height_Nov2022.csv: include Network_origin (TPSF/TF), Study, Country, Province, Disturbance, Forest_condition, Restorations measures, Planting_density, Planting_sp_no, Plot_id, Number_planted, Number_monitored, Duration_months, Species, Lat/lon, Wood density metrics, Sample_weight, and various planting and census details.
- Height-related fields include Height_0_v2 (initial planting height adjustments) and Height_cm_v2 (height at duration_months), plus derived AGR/ASGR-related fields.
- Additional fields provide model outputs (Model_AIC, Ref_height, SGR, AGR, AGRvar) for each treatment’s height trajectory.

## Licensing, accessibility, and limitations
- WorldClim covariates require separate download and are not embedded in the dataset due to licensing constraints.
- Data aggregation across studies and sites involves heterogeneity in measurement methods and reporting; users should account for varying sample sizes and monitoring durations.
- TF vs. TPSF contexts, disturbance types, and restoration measures influence comparability; appropriate stratification is recommended in analyses.
- Assumptions are eingebed in sampling weights where explicit numbers are missing (documented in the field descriptions).

## Publication reference
- This dataset accompanies Banin LF, Raine EH et al. (2023) The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.