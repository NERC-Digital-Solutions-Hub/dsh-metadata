# The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests

- Purpose and scope: A dataset of survival and heights of trees planted for forest restoration in South and Southeast Asia, accompanying Banin et al. (2023). Collated from published studies, grey literature, and co-authors, up to May 2021, across 176 sites where disturbance or clearance occurred and restoration planting was monitored over time. Used to model height growth, derive annual size-standardised growth rates (ASGR), and test effects of biophysical, climatic, and planting regime variables on survival and growth. Represents current knowledge on restoration outcomes in the region.

- Contents and structure:
  - Core data files:
    - df_study_details.csv: study and site details for height and/or survival datasets
    - df_survival_Nov2022.csv: survival data for planted trees
    - df_height_Nov2022.csv: height measurements from multiple censuses
  - Analysis and utility files:
    - script_SynthesisAnalysis_MortalityModels.R: R code for mortality (survival) analyses
    - height_nlm_functions.R: functions for fitting linear, exponential, and Gompertz models to height data
    - height_ASGR_nlms.R: code for height modeling, model selection, and ASGR calculation
    - script_SynthesisAnalysis_ASGR_MEMs.R: R code for ASGR-related analyses
    - Additional outputs: any AGR/SGR model outputs and related files
  - Supporting information:
    - supporting_info_survival_height.docx: data collection, preparation, processing, and analysis details
  - Adaptation note: Dataset created per Banin et al. (2023) protocols; analyses rely on external WorldClim climate layers (licensing prevents integration with the dataset) and Wood density data from Zanne et al. (2009) via the BIOMASS R package

- Data sources, scope, and timeframe:
  - Source types: published papers, grey literature, and data contributed by co-authors
  - Coverage: 176 sites across South and Southeast Asia
  - Timeframe: censuses up to May 2021
  - Location and context: sites located where natural forest disturbance occurred; seedlings planted and monitored to assess restoration outcomes

- Key data dependencies and licensing considerations:
  - Climate data: WorldClim 2.5 arc-minute layers (BIO1, BIO5, BIO6, BIO12, BIO16, BIO17, elevation) required for certain analyses; licensing prevents direct integration with dataset files
  - Wood density: species wood density data provided via the BIOMASS package (Zanne et al. 2009)
  - Reproduction of processed data workflows: run height_ASGR_nlms.R (depends on height_nlm_functions.R) to generate processed datasets; subsequent analyses via script_SynthesisAnalysis_ASGR_MEMs.R and script_SynthesisAnalysis_MortalityModels.R

- Field descriptors and core variables (highlights):
  - Study and site context:
    - Study, Country, Province
    - Forest type: TF (tropical forest on mineral soil) or TPSF (tropical peat swamp forest)
    - Disturbance: LG, AG, PL, F, M, DR
    - Forest_condition categories: Forest_enrichment, Plantation_enrichment, Open_degraded
  - Restoration and planting details:
    - Restoration measures: six binary columns (comp_removal, shading, soil_prep, water_reg, fertilisation, protection)
    - Planting_density: seedlings per hectare (across all species/treatments)
    - Planting_sp_no: total species planted in the treatment
    - Plot_id: identifier for a seedling group at a site with a given treatment
    - Number_planted, Number_monitored
    - Duration_months: time since planting
  - Plant material and geography:
    - Species_full, Genus, Species, Family
    - Lat_dec, lon_dec
    - W_meanWD, W_sdWD, W_levelWD, W_nInd
  - Survival dataset fields (survival-focused):
    - Age_0, Height_0: planting age and height (cm)
    - Survival_per: survival percentage at duration_months
    - Yr_cat: year category post-planting
    - Number_alive, Number_dead
  - Height dataset fields (growth-focused):
    - Height_0_v2: initial seedling height (including early measurements)
    - Height_cm_v2: height at subsequent census moments
    - Av_height0: whether initial height was assumed
  - Model outputs and growth metrics:
    - Model_AIC: best model type for mortality or height (e.g., lm, gomp, exp)
    - Ref_height: reference height in cm for growth rate calculations
    - SGR: instantaneous size-standardised growth rate at reference height
    - AGR: annual growth rate around the year of reaching the reference height
    - AGRvar: variance of AGR
    - Additional: Number of censuses (No_census), other AGR/ASGR-related outputs

- Intended use and benefits for data users:
  - Reproduce and extend analyses on restoration outcomes (survival and height growth) across biophysical and climatic conditions
  - Compare impacts of different restoration measures and planting regimes
  - Derive ASGR and other growth metrics to support biodiversity and carbon restoration planning
  - Use geospatial and species-level data to explore context-specific restoration performance

- Data quality, limitations, and notes:
  - Data are collated from diverse sources with varying reporting standards; reconciliation performed per Banin et al. 2023 protocols
  - Data quality and completeness vary by site and study; some fields may be inferred or require assumptions (e.g., sample weights, initial heights)
  - Licensing constraints limit integrating WorldClim climate layers directly within the dataset files
  - The dataset aims to represent the current knowledge base, not a single uniform experimental design; results should consider site-specific contexts

- Access and reproduction guidance:
  - To reproduce analyses, run height_ASGR_nlms.R (requires height_nlm_functions.R) to generate processed height datasets, then execute script_SynthesisAnalysis_ASGR_MEMs.R for ASGR analyses; mortality analyses via script_SynthesisAnalysis_MortalityModels.R
  - Reference the supporting_info_survival_height.docx for detailed data collection and processing methodologies and ensure appropriate citations to Banin et al. (2023) and the dataset citation in publications

- Provenance and citation:
  - Dataset accompanies Banin LF, Raine EH, et al. (2023) “The road to recovery: a synthesis of outcomes from ecosystem restoration in tropical and sub-tropical Asian forests” in Philosophical Transactions of the Royal Society B
  - Dataset and code provide a transparent, reproducible workflow aligning with the publication’s analyses and findings