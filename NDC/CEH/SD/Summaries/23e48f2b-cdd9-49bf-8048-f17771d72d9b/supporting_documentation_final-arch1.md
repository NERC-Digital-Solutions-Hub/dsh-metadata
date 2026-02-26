# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

- Provenance and context
  - Data originate from the Natural Laboratory of Peat-swamp Forest special research zone in Sebangau National Park, Central Kalimantan, Indonesia.
  - Forest type: ombrogenous, non-masting peat-swamp; history of selective logging until 1997 and illegal hand-logging until 2004, creating canals that drained peat and increased fire risk.
  - Purpose: test tree planting, including nursery propagation and outplanting, to evaluate survival and growth of native species under different planting conditions.

- Data collection overview
  - Nursery data (seedlings): two nurseries (established 2005 and 2010) within the research zone; conditions varied from forest-replica to forest-edge environments with shading nets to reduce herbivory; seedlings monitored for survival and height.
  - Seed sources and treatments: seeds collected from adjacent relatively undisturbed forest; 40 native tropical peat-swamp species from 29 genera; cohorts categorized by species, seedling origin (seedling vs wildling), and fertilization treatment (fertilised, non-fertilised, unknown).
  - Outplanting data: six small-scale trials with 24 species total; seedling vs wildling stock; varied site conditions (open old burns, open recent burns, forest edge, relatively undisturbed forest); planting treatments included bakul (weaved baskets), shade (roof), both, or none; monitoring spanned up to several years with 156 outplanted seedling cohorts.
  - Measurements: alive/dead status and height in cm for nursery and outplanting cohorts; additional details include basal diameter and leaf counts for individual-tree monitoring.
  - Precipitation data: daily rainfall from PERSIANN-CDR (0.25-degree grid) used to compute total precipitation for two-year periods post-planting to align with standardized growth calculations.

- Nature and units of recorded values
  - Units are specified in data tables accompanying the dataset; common units include:
    - Height: centimetres (cm)
    - Precipitation: millimetres (mm)
    - Time: days and months
    - Survival and mortality: percentages
  - Data files include both cohort-level summaries and individual-tree measurements.

- Data quality and standardization
  - Quality control: comprehensive observer training and refresher sessions; field-team leadership ensured consistency; data were screened for outliers, errors, typos, and missing values; cross-checks with field reports and observer names.
  - Taxonomy and naming: local names checked and corrected for spelling; Latin names assigned using Husson et al. (2018) with nomenclature aligned to APG IV and Taxonomic Name Resolution Service; unique tags used for reliable tracking of each seedling.

- Data structure (four CSV files)
  - Nursery_cohort_summary.csv
    - Summary survival and growth for nursery cohorts (same species, origin, and nutrient treatment entered in a given nursery month).
    - Key fields: species_local, species_latin, nursery_entry_year/month, origin, nutrients, final_duration_days_mean, survival_per_2yrs_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean/RGRm_sd, total_precip_mm, and other cohort-level metrics.
  - Nursery_individual_tree.csv
    - Individual nursery-tree monitoring data; one row per monitoring event per seedling (identified by tagN).
    - Key fields: tagN, origin, species_local/latin, nursery_entry_date, duration_days, height_cm, diam_basal_cm, number_leaves, survival, nutrients, batch_final.
  - Outplanting_cohort_summary.csv
    - Summary survival and growth for outplanting cohorts (defined by project, site, transect, species, and treatment).
    - Key fields: project, site, transect, site_broadcategory, species_local/latin, planting_treatment, planting_year/month, final_duration_days_mean, survival_per_2yrs_mean, number_planted, final_mortality_per_mean, half_life_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean/RGRm_sd, height0_mean, total_precip_mm, among others.
  - Outplanting_individual_tree.csv
    - Individual outplanted-tree monitoring data; one row per monitoring event per tree (tagN).
    - Key fields: project, site, transect, site description, transect, species_local/latin, planting_treatmen t, planting_date, monitoring_date, duration_days, duration_months, survival, height_cm, number_leaves, diam_basal_cm, etc.

- Analytical methods and standardization
  - Objective: derive comparable survival and height growth measures across nursery and outplanting cohorts with different monitoring durations, standardizing to two years (730 days).
  - Procedures:
    - Mortality-based survival at two years (survival_per_2yrs_mean) and related metrics (half_life_mean, final_mortality_per_mean) inferred via line fitting across time using linear, exponential, power-law, asymptotic, and logistic models; model selection via lowest Akaike Information Criterion (AIC) and R2 ≥ 0.5.
    - Height at two years (height_cm_2yrs_mean and height_cm_2yrs_sd) obtained from time-based height models; negative or >10 m predictions removed.
    - Relative growth rate (RGRm_mean and RGRm_sd) estimated at the two-year point using linear and non-linear models; RGR expressed as cm per cm per day.
  - Special handling:
    - Cohorts with 0% mortality that did not change were set to 100% survival if monitoring extended beyond two years.
    - For outplanting, some cohorts received NA values where robust two-year predictions were not possible (e.g., insufficient temporal replication or poor model fit, R2 < 0.5).
  - Precipitation integration: two-year total precipitation (total_precip_mm) calculated from PERSIANN-CDR data to align with standardized survival and growth estimates.

- References and methodological foundation
  - Line-fitting standardization approach follows Smith et al. (2022); mortality and growth modeling drawn from approaches in Paine et al. (2012) and related ecological growth-model literature.
  - Taxonomic and botanical references used for species identification and naming, including Angiosperm Phylogeny Group (APG IV) classification.
  - Data provenance and relevant literature cited throughout (e.g., Harrison et al. 2023 on cumulative seedling performance from nursery to outplanting).

- Associated publication
  - This Supporting Information and the accompanying datasets relate to Harrison et al. (2023): Accounting for cumulative seedling performance from nursery to outplanting when reforesting degraded tropical peatlands (Restoration Ecology).