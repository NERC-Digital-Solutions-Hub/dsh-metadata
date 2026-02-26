# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Overview
- Comprehensive dataset accompanying Banin et al. (2023) on forest restoration outcomes in tropical and subtropical Asia.
- Focuses on survival and height of trees planted for restoration, collated from published studies, grey literature, and co-author data up to May 2021.
- Covers 176 sites where disturbance/clearance occurred, with trees planted and monitored over time.
- Analyses model height growth, extract annual size-standardised growth rates (ASGR), and test effects of biophysical, climatic conditions, and planting regimes on survival and growth.
- Created to reflect current knowledge on restoration outcomes in South and Southeast Asia; this is the full dataset for the survival and height analysis.

## Datasets and contents
- df_study_details.csv: study and site details for height and/or survival analyses.
- df_survival_Nov2022.csv: survival data for planted trees.
- df_height_Nov2022.csv: height data from multiple censuses.
- script_SynthesisAnalysis_MortalityModels.R: mortality analysis scripts.
- height_nlm_functions.R: functions for fitting linear, exponential, and Gompertz height models.
- height_ASGR_nlms.R: code for fitting height models, model selection, and calculating ASGR.
- script_SynthesisAnalysis_ASGR_MEMs.R: statistical analysis of height using ASGR and MEMs.
- supporting_info_survival_height.docx: data collection, preparation, processing, and analysis details (adapted from Banin et al. 2023).
- Adapted from Banin et al. (2023) manuscript materials.

## Data collection, provenance, and scope
- Data collated following Banin et al. 2023 protocols and supplementary materials.
- Sources include published papers, grey literature, and data contributed by co-authors.
- Forest types: TF (tropical forest on mineral soil) and TPSF (tropical peat swamp forest).
- Disturbance categories include logged, agriculture, plantation, fire, mining, and drained.
- Restoration measures captured as binary fields across six categories (e.g., removal of competition, shading, soil preparation, water regulation, fertilisation, protection).
- Planting_context and demographic fields capture planting density, species composition, site conditions, and census details.

## Data structure and field descriptors
- Survival dataset fields (df_survival_Nov2022.csv): country, province, site identifiers (UIC), study, disturbance, forest condition, restoration treatment, planting density and species, census duration, age and height at planting, survival percentages, numbers alive/dead, and year categories.
- Height dataset fields (df_height_Nov2022.csv): height at planting (Height_0_v2), height at census (Height_cm_v2), initial height assumptions (Av_height0), site and treatment metadata, census count, and model outputs (see below).
- Site and species descriptors include latitude/longitude, forest type, plot identifiers (Plot_id), restoration treatment status, and planting counts.
- Wood density data: Sourced from Zanne et al. (2009) via the BIOMASS R package; used as context for species traits.
- Additional fields for growth modeling (provided by AGR model outputs): Model_AIC, Ref_height (100/200/300 cm), SGR (instantaneous growth rate), AGR (annual growth rate), AGRvar, No_census.

## Processing, models, and reproducibility
- Core analyses require running:
  - height_ASGR_nlms.R to fit models and generate processed height datasets.
  - height_nlm_functions.R as dependencies for model fitting (linear, Gompertz, exponential).
  - script_SynthesisAnalysis_ASGR_MEMs.R for ASGR-based analyses.
  - script_SynthesisAnalysis_MortalityModels.R for mortality modeling.
- WorldClim data dependencies (2.5 arc-minute resolution) are needed for bioclimatic predictors:
  - vals_temp (annual mean temp), vals_maxTwm (max temp of warmest month), vals_minTcm (min temp of coldest month), vals_precip (annual precipitation), vals_pwq (precipitation of wettest quarter), vals_pdq (precipitation of driest quarter), vals_elev (elevation).
  - Note: WorldClim data cannot be integrated directly with this dataset due to licensing restrictions.
- Field and processing notes:
  - Distinct data processing rules for survival and height datasets, including treatment-level aggregation and assumptions about numbers monitored when not reported.
  - Height modeling outputs include model choice (lm, gomp, exp), reference height, and growth metrics (SGR, AGR, AGRvar).

## Licensing, dependencies, and data governance
- WorldClim data licensing prevents direct integration; users must obtain their own licensed climate layers for reproducibility beyond this dataset.
- Field and methodological provenance are aligned with Banin et al. (2023) and accompanying supplementary materials.
- Documentation notes that the dataset is a complete compilation up to May 2021, with subsequent analysis (Nov 2022 versions of survival/height files) reflecting updates or revisions.
- Wood density and other trait data derive from published sources; consistency across sites relies on standardized field descriptors and coding in the provided CSVs.

## Data quality, caveats, and stewardship considerations
- Heterogeneity across sites, studies, and measurement protocols; standardization efforts are described but residual comparability challenges may exist.
- Several fields rely on assumptions or equal partitioning when explicit counts are missing (e.g., Number_monitored, sample_weight), which should be considered in analyses and repurposing.
- Spatial and environmental covariates are optional/conditional due to licensing; users needing climate covariates must manage licensed data separately.
- The dataset provides a robust, transparent lineage: original sources, protocols, processing scripts, and model outputs are all included to support reproducibility and governance.

## Citation, usage, and access notes
- Please cite Banin Lindsay F., Raine Elizabeth H., Rowland Lucy M., et al. 2023, Survival and heights of trees planted for forest restoration in South and Southeast Asia. NERC-Environmental Information Data Centre (dataset) and accompanying publication: The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests. Philosophical Transactions of the Royal Society B.
- Data are designed to enable replication of the mortality and height analyses and to support meta-analyses of restoration outcomes across South and Southeast Asia.
- For access to code and datasets, refer to the included R scripts and CSV files; ensure licensing for external climate data is respected.