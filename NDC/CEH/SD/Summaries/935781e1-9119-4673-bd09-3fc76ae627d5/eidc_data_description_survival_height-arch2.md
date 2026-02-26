# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Overview
- A dataset accompanying Banin et al. (2023) on forest restoration outcomes in tropical South and Southeast Asia.
- Focuses on survival and height of trees planted for restoration, with analytical code to reproduce the analyses in the associated publication.
- Aimed at representing the current knowledge base for restoration outcomes and enabling monitoring of environmental restoration over time.

## What the dataset contains
- Tree survival and height data from 176 planting sites where disturbance or clearance occurred prior to restoration.
- Time series data covering multiple censuses per treatment, up to May 2021.
- Standardised outputs including survival rates, height growth, and annual growth metrics (ASGR) across biophysical, climatic, and planting regime variables.
- Associated analytical code and documentation to reproduce analyses.

## Data sources and scope
- Data collected from:
  - Published studies
  - Grey literature
  - Data contribution from co-authors
- Sites span South and Southeast Asia; disturbances include agriculture, logging, mining, fire, drainage, and plantations.
- Plantings involve multiple species and restoration treatments, with detailed site and treatment descriptors.

## Files and structure
- df_study_details.csv: study and site details for height and/or survival datasets.
- df_survival_Nov2022.csv: survival data by treatment/site.
- df_height_Nov2022.csv: height measurements across censuses.
- script_SynthesisAnalysis_MortalityModels.R: mortality analysis code.
- height_nlm_functions.R: functions for nonlinear model fitting (linear, exponential, Gompertz) of height data.
- height_ASGR_nlms.R: code for fitting height models, model selection, and calculating ASGR.
- script_SynthesisAnalysis_ASGR_MEMs.R: statistical analysis code for ASGR and related metrics.
- supporting_info_survival_height.docx: data collection, processing, and analysis details.
- Adaptation notes: dependencies and data processing steps aligned with Banin et al. (2023) methods.

## Analytical workflow and dependencies
- Dependencies: height_ASGR_nlms.R relies on height_nlm_functions.R to produce processed datasets.
- Primary analyses:
  - Mortality models (survival data) and height growth analyses.
  - Calculation of annual size-standardised growth rate (ASGR) and related metrics.
- Climate data integration:
  - WorldClim 2.5 arc-minute layers required for several analyses (BIO1, BIO5, BIO6, BIO12, BIO16, BIO17, elevation).
  - Data extraction by site is necessary, but licensing prevents integrating WorldClim layers directly within the dataset package.
- Wood density: values from Zanne et al. (2009) via BIOMASS R package, used in modeling.

## Key variables and field descriptors
- Study-level (df_study_details.csv):
  - Forest_type: TF (tropical forest on mineral soil) or TPSF (tropical peat swamp forest)
  - UIC: unique site identifier within studies
  - Reference: full citation of the contributing paper
- Survival dataset (df_survival_Nov2022.csv):
  - Network_origin: TF or TPSF
  - Study, Country, Province
  - Disturbance and Forest_condition classifications (e.g., logged, agriculture, plantation, open_degraded, etc.)
  - Restoration measures and planting_density/planting_sp_no
  - Plot_id, Duration_months, Age_0, Height_0, Survival_per, Number_alive, Number_dead
  - Species information (Species_full, Genus, Species, Family)
  - Location (Lat_dec, lon_dec), Wood density data (W_meanWD, W_sdWD, etc.)
- Height dataset (df_height_Nov2022.csv):
  - Height_0_v2, Height_cm_v2: planting and census heights
  - Av_height0: whether initial height is assumed
  - Duration_months, Census_last, Number_monitored, Number_alive/Dead (where applicable)
- Additional model outputs (AGR/ASGR):
  - Model_AIC, Ref_height, SGR, AGR, AGRvar, No_census, Duration_months

## How this supports environmental monitoring and policy evaluation
- Provides a harmonised, multi-site dataset to compare restoration outcomes across regions, species, and management practices.
- Enables standardised reporting of survival and growth over time, supporting assessments of restoration success and policy impact.
- Facilitates data integration with external datasets (subject to licensing) to enhance cross-cutting environmental health monitoring.
- Offers reproducible analytical workflows to stakeholders for benchmarking and long-term monitoring.

## Data quality, limitations, and caveats
- Data collated from diverse sources with varying methodologies; standardisation aims to enable cross-site comparisons.
- WorldClim data used for climate variables are not embedded due to licensing; site-level climate data must be downloaded separately for analyses.
- Some fields rely on assumptions (e.g., sample weights, initial heights) when explicit values are missing; these are documented in the supporting materials.
- The dataset represents the state of knowledge up to May 2021; newer data may extend or update findings.

## Usage notes and access
- Data and code are provided to reproduce mortality and growth analyses as reported in Banin et al. (2023).
- Users should cite Banin et al. (2023) alongside this dataset when used for scholarly work.
- WorldClim data licensing restricts direct integration within the dataset; users should source these climatic layers independently if needed for analyses.

## Citation and provenance
- Publication: Banin LF, Raine EH et al. 2023. Survival and heights of trees planted for forest restoration in South and Southeast Asia. NERC-Environmental Information Data Centre.
- This dataset is the full data underpinning the stated analyses, including raw and processed data, and the analytical scripts used to derive mortality and growth metrics.