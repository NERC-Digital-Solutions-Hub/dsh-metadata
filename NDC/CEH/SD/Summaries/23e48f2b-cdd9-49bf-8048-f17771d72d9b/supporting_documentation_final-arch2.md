# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

## Purpose and scope
- Provides standardized, cumulative measures of seedling performance from nursery to outplanting to support monitoring of environmental restoration in a degraded tropical peatland.
- Data designed for scrutiny of environmental health and restoration policy performance over time.

## Provenance and study context
- Location: Natural Laboratory of Peat-swamp Forest, Sebangau National Park, Central Kalimantan, Indonesia.
- Environment: Ombrogenous, non-masting peat-swamp forest with a history of selective logging (until 1997) and illegal hand logging (until 2004); small canals caused peat drainage and fire risk.
- Reforestation trials: Nursery propagation and outplanting trials across six project names, testing native species under different nursery and site treatments.
- Species: 40 native tropical peat-swamp forest species from 29 genera.

## Data collected and datasets
- Seedling nursery data from two nurseries (2005–2014 collection period) reflecting forest-like conditions and edge conditions.
- Six outplanting trials with diverse species mixes (total 24 species; mean 7 per trial; 2–11 per trial) and site conditions (open old burn, open recent burn, forest edge, relatively undisturbed forest).
- Precipitation data: daily precipitation from PERSIANN-CDR for standardizing 2-year growth and survival analyses.
- Datasets capture both nursery-level and outplanting-level performance, including survival and height over time.

## Nursery data
- Seedling nursery operations: two nurseries located at Sebangau; one inside forest and one near forest edge; shading nets used to reduce herbivore damage and simulate natural rainfall exposure.
- Seedling origin and treatments: seeds collected locally; cohorts defined by species, origin (seedling vs wildling), and fertilisation status (fertilised, non-fertilised, unknown).
- Monitoring: survival and height (cm) recorded; cohorts tracked monthly to capture growth dynamics.
- Coverage: nursery data for 40 species across 97 seedling cohorts (grouped by species, origin, treatment, entry month).

## Outplanting data
- Six outplanting projects (RF-2012, RF-2013, RG-2009, DH-2014, LH-2016, BFA-2016) with diverse site conditions and planting treatments.
- Outplanting monitoring: survival and height measured for cohorts over multiple time points; plots/transects defined per project and site condition.
- Site conditions and treatments: open old burn, open edge, forest edge, and varying burn histories; treatments include bakul baskets, shade structures, both, or control.
- Cohorts defined by species, site condition, treatment, and plot/transect; 156 outplanted seedling cohorts across trials.

## Data file structures (Four CSV files)
- Nursery_cohort_summary.csv: summary survival and growth for nursery cohorts (grouped by species, origin, nutrient treatment, and entry month). Key outputs include:
  - Survival at two years (survival_per_2yrs_mean)
  - Final mortality (final_mortality_per_mean)
  - Height at two years (height_cm_2yrs_mean, height_cm_2yrs_sd)
  - Relative growth rate (RGRm_mean, RGRm_sd)
  - Total precipitation over 2 years (total_precip_mm)
  - Other cohort-level metrics (e.g., duration, number planted)
- Nursery_individual_tree.csv: individual nursery monitoring data (per monitoring event) including tagN, height, basal diameter, leaves, survival, nutrients, and batch identifiers.
- Outplanting_cohort_summary.csv: summary survival and growth for outplanting cohorts (project, site, transect, site_broadcategory, species, planting_treatment, planting_year/month). Key outputs mirror nursery cohort metrics:
  - Survival_per_2yrs_mean, final_mortality_per_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean, RGRm_sd
  - Number planted, final heights, and precipitation
  - Variables describing site and treatment
- Outplanting_individual_tree.csv: individual outplanted tree monitoring data (per monitoring event) including project, site, transect, tagN, species, planting_treatment, planting_date, monitoring_date, duration, survival, height, leaves, basal diameter, etc.

## Data collection methods
- Nurseries: two facilities with shade, netting, and exposure to natural rainfall to simulate field conditions; one located deeper in forest, one near the edge.
- Outplanting trials: six projects with detailed site characteristics, planting density, seedling origin, and monitoring schedules. Projects include RG-2009, RF-2012, RF-2013, DH-2014, LH-2016, and BFA-2016, each with specific coordinates, burn history, edge distance, and flooding classification.
- Weather data: daily precipitation sourced from PERSIANN-CDR (GridSat-B1 infrared data) to compute total precipitation for two years post-planting.

## Quality control and data management
- Rigorous observer training for nursery and field staff; ongoing refresher training; field lead maintained continuity.
- Data screening for outliers, typos, missing values, and questionable dates; cross-checked with monthly field reports and field team notes.
- Negative height growth scrutinized, due to incidents of snapping and regrowth; all observer names recorded on data sheets.
- Species identification standardized to Latin names using recognized references; local names cross-checked for consistency.
- Unique tags used for both nursery and outplanting to ensure traceability of individuals and cohorts.

## Analytical methods and standardization
- Standardization approach: line-fitting to mortality and growth time series to estimate comparable 2-year metrics (730 days) across cohorts with varying monitoring durations.
- Outputs and modeling:
  - Survival at 2 years (survival_per_2yrs_mean), half-life (half_life_mean), final mortality (final_mortality_per_mean) derived from mortality models (linear, exponential, power-law, asymptotic, logistic) chosen by lowest AIC; models with R2 < 0.5 removed; 0% mortality cohorts with no change manually set to 100% survival after two years.
  - Height at 2 years (height_cm_2yrs_mean, height_cm_2yrs_sd) derived from height-time fits; negative values or >10 m removed.
  - Relative growth rate at 2 years (RGRm_mean, RGRm_sd) computed using linear or non-linear fits; RGR units are cm per cm per day.
- For outplanting: similar standardized metrics (with NA when data insufficient for line fitting).
- Precipitation (total_precip_mm) used as a covariate in growth/survival modeling and reporting.
- References and methods are aligned with established approaches (e.g., Smith et al. 2022; Paine et al. 2012).

## Relevance for environmental monitoring and policy
- Enables assessment of cumulative performance from nursery to field, informing restoration effectiveness and adaptive management.
- Standardized 2-year survival and growth metrics support temporal comparisons and policy evaluation across projects, site conditions, and treatments.
- Data quality practices and provenance support reproducibility and integration with other environmental monitoring datasets.

## References (selected)
- Methods for standardization and line-fitting (Smith et al. 2022; Paine et al. 2012).
- Taxonomy and species identification references; field guides and APG IV framework for plant names.
- Data sources for precipitation: PERSIANN-CDR and GridSat-B1 data products.
- Related restoration ecology and peatland literature detailing seedling performance and canopy recovery in tropical peat swamps.