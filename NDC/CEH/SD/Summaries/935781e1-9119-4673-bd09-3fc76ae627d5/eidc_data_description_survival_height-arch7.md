# The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

## Overview
- Dataset documenting survival and heights of trees planted for forest restoration in South and Southeast Asia.
- Includes 176 sites, with planting and monitoring data up to May 2021, across disturbed sites undergoing restoration.
- Analyses focus on height growth, annual size-standardised growth rates (ASGR), and the influence of biophysical, climatic conditions and planting regimes on survival and growth.
- Aimed at representing the current state of knowledge on restoration outcomes in the region.

## Data content and structure
- Files and purposes
  - df_study_details.csv: study/site details for height and/or survival datasets.
  - df_survival_Nov2022.csv: survival data for planted trees.
  - df_height_Nov2022.csv: tree height data from multiple censuses.
  - script_SynthesisAnalysis_MortalityModels.R: mortality analysis code.
  - height_nlm_functions.R: functions for fitting height growth models (linear, exponential, Gompertz).
  - height_ASGR_nlms.R: code for height modeling, model selection, ASGR calculations.
  - script_SynthesisAnalysis_ASGR_MEMs.R: statistical analysis for ASGR and related models.
  - supporting_info_survival_height.docx: data collection, processing and analysis details.
- Data provenance
  - Collated from published studies, grey literature and co-authors; up to 2021.
  - 176 sites where disturbance occurred prior to planting and subsequent monitoring.

## Spatial, temporal and biophysical context
- Location fields: Lat_dec, lon_dec; Country, Province.
- Forest types: TF (tropical forest on mineral soil) or TPSF (tropical peat swamp forest).
- Disturbance types: logged, agriculture, plantation, fire, mining, drained.
- Restoration context: 
  - Forest_condition categories (Forest_enrichment, Plantation_enrichment, Open_degraded).
  - Six binary restoration measures (comp_removal, shading, soil_prep, water_reg, fertilisation, protection) and related activity details.
- Planting details: planting_density (seedlings per hectare), Planting_sp_no (species planted), Number_planted, Number_monitored, Plot_id.
- Species data: Species_full, Genus, Species, Family; wood density data (W_meanWD, W_sdWD, W_levelWD, W_nInd) tied to BIOMASS/Zanne et al. (2009).
- Temporal data: Duration_months since planting; Age_0 and Height_0 at planting; Height_cm_v2 by census; Survival_per with corresponding alive/dead counts.
- Field descriptors for height: Height_0_v2 (initial height), Av_height0 (assumed average initial height where needed).
- Sampling and weighting: Sample_weight and Sample_assumption describe how sample sizes are inferred when not explicitly reported.
- Spatial and climatic context: WorldClim-derived climate variables used in analyses (annual mean temperature, warmest/coldest month temperatures, annual precipitation, precipitation of wettest/driest quarters) but not included directly due to licensing.

## Processing, dependencies and licensing
- Analyses requiring WorldClim data layers (2.5 arc-minute) must be downloaded separately; these data cannot be embedded due to licensing.
- Required processing steps:
  - Run height_ASGR_nlms.R (depends on height_nlm_functions.R) to generate processed height datasets.
  - Run script_SynthesisAnalysis_ASGR_MEMs.R for ASGR analyses.
  - Run script_SynthesisAnalysis_MortalityModels.R for mortality models.
- Wood density data sourced from Zanne et al. (2009) via the BIOMASS R package.

## GIS-specific uses
- Mapping opportunities:
  - Visualise survival percentages and alive/dead counts by site and treatment.
  - Map height trajectories and ASGR across species, sites and restoration regimes.
  - Overlay with climate, elevation and disturbance overlays (via separate WorldClim layers and site coordinates).
- Attribute-rich analyses:
  - Explore relationships between survival/growth and forest type, disturbance category, restoration measures, planting density, and species.
  - Examine biophysical and climatic correlations with outcomes (requires external WorldClim data).
  - Compare outcomes across TF and TPSF sites, and across different restoration strategies.

## Limitations and considerations
- WorldClim data not included; external access required for climate analyses.
- Some sample sizes are inferred through assumptions (sample_weight) when explicit numbers are missing.
- Dataset emphasizes tropical and subtropical Asia; caution in generalising beyond region or forest types.
- Variation in recording conventions between TF and TPSF sites.

## Reproducibility and provenance
- Dataset reflects Banin et al. (2023) work; dataset accompanies the publication “The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests.”
- Proper citation recommended for both dataset and publication.

## Access and usage notes
- Contents include detailed study and site metadata, survival and height datasets, and analysis scripts.
- Supporting information provides data collection, preparation, processing and analysis details.
- Use in conjunction with the publication to inform restoration planning, policy, and spatial planning initiatives through GIS-based visualization and analysis.