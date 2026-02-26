# Survival and heights of trees planted for forest restoration in South and Southeast Asia

## Purpose and scope
- A dataset accompanying Banin et al. (2023) that documents survival and height of trees planted for forest restoration in South and Southeast Asia.
- Synthesises outcomes from 176 planting sites where disturbance occurred and forests were restored by planting, monitored over time.
- Supports analysis of height growth, annual size-standardised growth rates (ASGR), and the effects of biophysical/climatic conditions and planting regimes on survival and growth.
- Includes both raw data (survival and heights) and analytical code to reproduce the analyses reported in the related publication.

## Data content and structure
- Main data files:
  - df_study_details.csv: study/site level details for height/survival analyses.
  - df_survival_Nov2022.csv: survival data by treatment/site.
  - df_height_Nov2022.csv: height data across censuses.
- Analytic and support files:
  - script_SynthesisAnalysis_MortalityModels.R: mortality modeling code.
  - height_nlm_functions.R: functions for fitting height models (linear, exponential, Gompertz).
  - height_ASGR_nlms.R: code for height growth modelling and ASGR calculations.
  - script_SynthesisAnalysis_ASGR_MEMs.R: statistical analysis for ASGR/MEm-based models.
  - supporting_info_survival_height.docx: data collection, preparation, processing, and analysis details.
- The dataset and protocols follow Banin et al. (2023) main text and supplementary materials.

## Data content and metadata details
- Field types cover: forest type (TF or TPSF), site identifiers (UIC), country/region, disturbance type, restoration measures, planting density and species richness, plot-level treatment design, census timing, survival counts, seedling height measurements, planting age, initial height (Height_0 or Height_0_v2), and derived metrics like Survival_per, SGR, and AGR.
- Species and functional information: Genus, Species, Family; wood density data ( sourced from Zanne et al. via the BIOMASS R package).
- Spatial and environmental context: latitude/longitude, WorldClim-derived climate variables (used in modelling; see dependencies), elevation.
- Sampling and data handling: sample weights, assumptions, site/species combinations, and fields describing whether a census is the last in a treatment.
- Data coding for restoration measures includes six binary columns (e.g., comp_removal, shading, soil_prep, water_reg, fertilisation, protection) indicating implementation (1) or not (0).

## Processing, replication, and dependencies
- Reproduction of analyses requires:
  - height_ASGR_nlms.R (and height_nlm_functions.R) to generate processed height datasets.
  - script_SynthesisAnalysis_ASGR_MEMs.R for ASGR analyses.
  - script_SynthesisAnalysis_MortalityModels.R for mortality modelling (requires WorldClim environmental layers at 2.5 arc-minute resolution).
- WorldClim data are external to this dataset due to licensing restrictions and cannot be integrated directly with this dataset; climate variables used include annual mean temperature, warmest/coldest month temperatures, annual precipitation, precipitation of wettest/driest quarters, and elevation.
- Wood density data are provided (via BIOMASS/Zanne et al. 2009) and used in analyses where applicable.

## Data governance, quality, and accessibility considerations
- Metadata-rich dataset with explicit field definitions (e.g., Disturbance categories, Restoration categories, Site/plot identifiers, census timing).
- Transparent notes on sampling effort, weighting, and assumptions (e.g., sample_weight, Sample_assumption).
- Clear documentation of dependencies and reproducibility steps to enable auditability and policy-relevant monitoring.
- Licensing constraints on external WorldClim data mean full integration with climate layers is not contained within this dataset; data and code are provided to enable external linkage if licensing allows.

## Relevance for monitoring frameworks and policy
- Provides Metrics and Indicators for environmental health monitoring and restoration effectiveness:
  - Survival rates by species, site, disturbance, and restoration treatment.
  - Height growth trajectories and instantaneous growth rates (SGR), ASGR, and annual growth rates (AGR) linked to planting regimes and biophysical conditions.
  - Evaluation of restoration measures (e.g., competition removal, shading, soil preparation, water regulation, fertilisation, protection) on outcomes.
- Enables cross-site synthesis and benchmarking across tropical forests in South/Southeast Asia, informing policy decisions on restoration strategies, resource allocation, and monitoring design.
- Includes data governance considerations (data sharing, metadata quality, transparency) aligned with responsible monitoring framework practices.

## Practical considerations for policymakers and researchers
- Data and code are provided to enable replication, updating with new censuses, and re-analysis under different modelling assumptions.
- For climate-related analyses, external licensing of climate data (WorldClim) must be considered; use of the published variables within this dataset requires appropriate licensing and linking to external data sources.
- The dataset distinguishes forest types (TF vs TPSF) and disturbance categories, facilitating policy-relevant comparisons across restoration contexts.
- Clear guidance is available for citing the dataset and the associated Banin et al. (2023) publication when using the data.