# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Overview
- Dataset accompanying Banin et al. (2023) on forest restoration outcomes in South and Southeast Asia.
- Contains survival data and tree height measurements for planted trees across 176 sites with disturbances or clearance prior to planting.
- Covers multiple years of monitoring up to May 2021; compiled from published studies, grey literature, and co-authors.
- Aims to model height growth, extract annual size-standardised growth rates (ASGR), and test effects of biophysical/climatic conditions and planting regimes on survival and growth.
- Designed to represent current knowledge on restoration outcomes; used to support analyses in the associated publication.

## Data scope and structure
- Geographic and ecological scope: South and Southeast Asia; forest disturbances include logged, agricultural, plantation, fire, mining, and drainage impacts; forest types mainly tropical forest on mineral soil (TF) and tropical peat swamp forest (TPSF).
- Contents span both survival and height datasets, with accompanying metadata and coding to support replication and extended analyses.
- Related fields describe planting regimes, restoration measures, species, site conditions, and census timing.

## Files and their purposes
- df_study_details.csv — Details of studies/sites included in height and/or survival datasets.
- df_survival_Nov2022.csv — Survival data for planted trees.
- df_height_Nov2022.csv — Height measurements from multiple censuses.
- script_SynthesisAnalysis_MortalityModels.R — R code for mortality analyses (survival models).
- height_nlm_functions.R — Functions for fitting linear, exponential, and Gompertz height models.
- height_ASGR_nlms.R — Code for fitting height models, model selection, and calculating ASGR.
- script_SynthesisAnalysis_ASGR_MEMs.R — R code for ASGR-related analyses.
- supporting_info_survival_height.docx — Data collection, preparation, processing, and analysis details.
- Adapted procedures reference the Banin et al. (2023) manuscript and supplementary materials for data collation and processing.

## Data provenance and standards
- Data collated following protocols described in Banin et al. (2023) and dataset supplementary materials.
- Wood density data from Zanne et al. (2009) via the BIOMASS R package; WorldClim variables used in analyses but not integrated into the dataset due to licensing.
- WorldClim dependencies (2.5 arc-minute layers) required for certain analyses but not bundled in the dataset:
  - vals_temp (annual mean temperature)
  - vals_maxTwm (max temp of warmest month)
  - vals_minTcm (min temp of coldest month)
  - vals_precip (annual precipitation)
  - vals_pwq (precipitation of wettest quarter)
  - vals_pdq (precipitation of driest quarter)
  - vals_elev (elevation)

## Data fields and coding highlights
- Field descriptors cover:
  - Forest_type (TF or TPSF), Disturbance, Forest_condition, and Restoration measures (six 0/1 binary columns for various practices like removal of competition, shading, soil preparation, water regulation, fertilisation, protection).
  - Planting_density, Planting_sp_no, Plot_id, Number_planted/Number_monitored, Duration_months.
  - Species information (Species_full, Genus, Species, Family) and geographic identifiers (Country, Province, Lat_dec, lon_dec).
  - Biophysical covariates (W_meanWD, W_sdWD, W_levelWD, W_nInd) and sampling metadata (Sample_weight, Sample_assumption).
  - Survival-focused fields (Age_0, Height_0, Survival_per, Yr_cat, Number_alive, Number_dead).
  - Height-focused fields (Height_0_v2, Height_cm_v2, Av_height0) and model outputs (Model_AIC, Ref_height, SGR, AGR, AGRvar, No_census, Duration_months).
- Site-level and treatment-level identifiers:
  - UIC (unique site identifier within studies), Site_sp, Treatment, Census_last.
  - Disturbance codes and restoration category interpretations (e.g., Open_degraded, Plantation_enrichment, Forest_enrichment).

## Modeling, outputs, and usage
- Mortality models and height-growth modeling (linear, exponential, Gompertz) generate:
  - Best-fit model (Model_AIC), reference height, SGR, AGR, and associated uncertainty (AGRvar).
  - Temporal context for when reference heights are reached (Duration_months).
- Outputs are designed to support cross-site comparisons, sensitivity analyses, and policy-relevant synthesis of restoration outcomes.

## Licensing, access, and governance
- Primary data are compiled from multiple sources with protocols aligned to Banin et al. 2023; licensing restrictions apply to integrated external data (WorldClim layers) that cannot be embedded in the dataset.
- WOOD density data derived from published sources (Zanne et al. 2009) via BIOMASS in R.
- Clear provenance is provided via documentation and supplementary material to enable reproducibility and reuse.

## Reproducibility and data governance for Data Leaders
- Reproducibility:
  - Analyses require sequential execution of R scripts (e.g., height_ASGR_nlms.R depends on height_nlm_functions.R).
  - WorldClim data layers must be downloaded separately due to licensing; cannot be re-integrated directly with the dataset files.
- Data quality and gaps:
  - Data compiled from diverse studies and publication sources; potential heterogeneity in measurement protocols and missing data across sites.
  - Some fields include assumptions (e.g., Sample_weight defaults) and category definitions (e.g., Restorations measures) that require careful interpretation.
- Discoverability and maintenance:
  - Dataset structure with clearly named files and detailed field descriptions supports discoverability and reuse.
  - Documentation links to the companion publication and supplementary materials for consistent methodology.

## Practical takeaways for data strategy
- The dataset exemplifies a multi-source, harmonized dataset for ecosystem restoration outcomes, suitable for cross-site meta-analyses and policy-oriented insights.
- Key governance needs include:
  - Clear versioning and provenance trails to track updates (Nov 2022 updates for survival/height data and analyses).
  - Documentation of licensing constraints on external data layers and how to reproduce analyses with/without those layers.
  - Ongoing curation of site and treatment identifiers to maintain consistency across studies.
- Potential uses align with data-driven evaluation of restoration strategies, informing best practices in planting density, restoration measures, and species selection under varying biophysical and climatic conditions.