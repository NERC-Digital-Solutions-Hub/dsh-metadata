# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

- Overview
  - Supporting information set accompanying Harrison et al. (2023) detailing longitudinal nursery and outplanting data from Sebangau National Park, Central Kalimantan, Indonesia.
  - Focus on native tropical peat-swamp forest tree species, nursery growth, and outplanting survival and growth across six small-scale trials (2009–2016).
  - Data linked to a broader context of reforestation in degraded tropical peatlands; readers encouraged to consult Harrison et al. (2023) for interpretation.

- Provenance and study context
  - Collected in the Natural Laboratory of Peat-swamp Forest research zone.
  - Site history includes selective logging, canals causing drainage and fire risk, and subsequent reforestation trials with nursery and outplanting activities.
  - Nursery data: seeds and wildlings sourced from adjacent relatively undisturbed forest; seedlings tagged and monitored for survival and height under different fertilization treatments (fertilised, non-fertilised, unknown).
  - Outplanting data: six trials with various species mixes (24 species total), seedling vs wildling origin, and site conditions, including both plastic polybags and baskets ('bakul'). Monitoring included survival and height over time.
  - Precipitation data for two-year period used to contextualize growth and survival (PERSIANN-CDR).

- Data collected and scope
  - Nursery data (Dec 2009–Feb 2014) for 40 species from 29 genera; 97 nursery cohorts defined by species, origin, and fertilization treatment.
  - Outplanting data across six trials (RF-2012, RF-2013, DH-2014, LH-2016, BFA-2016, LH-2016 and related datasets) with 156 outplanted seedling cohorts.
  - Two seedling nurseries used: one within forest and one near forest edge; environmental conditions simulated for nursery and field outplanting.

- Data structure and files
  - Nursery_cohort_summary.csv: cohort-level summaries including
    - survival_per_2yrs_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean/sd, final_mortality_per_mean, half_life_mean, height_final_mean/sd, total_precip_mm, and other cohort descriptors (species_local, species_latin, origin, nutrients, entry date, etc.).
  - Nursery_individual_tree.csv: per-seedling nursery monitoring data with tagN, origin, species_local/latin, nursery_entry_date, duration_days, height_cm, diam_basal_cm, number_leaves, survival, nutrients, batch_final.
  - Outplanting_cohort_summary.csv: cohort-level summaries for outplanting projects including project, site, transect, site_broadcategory, species, planting_treatment, planting_year/month, final_duration_days_mean, survival_per_2yrs_mean, number_planted, final_mortality_per_mean, half_life_mean, height_cm_2yrs_mean/sd, RGRm_mean/sd, height0_mean, total_precip_mm.
  - Outplanting_individual_tree.csv: per-seedling outplanting monitoring data with project, site, transect, tagN, species, planting_treatment, planting_date, monitoring_date, duration_days/months, survival, height_cm, number_leaves, diam_basal_cm, etc.

- Data collection methods and monitoring
  - Two nurseries: one inside forest (to simulate forest conditions) and one near forest edge (to reflect post-planting conditions); shading and rainfall exposure implemented via netting.
  - Six outplanting trials with varied site conditions (open old burn, open recent burn, forest edge, relatively undisturbed forest) and plantings (seed/wilding origin, bakul shading, roofs, combinations, or controls).
  - Monitoring intervals ranged from monthly to annual depending on project, with standardized tagging and careful tracking of individual cohorts.

- Data standards, quality control, and processing
  - Data quality ensured via: trained observers, regular refresher training, field leadership (Salahuddin), and cross-checks with monthly field reports.
  - Outliers, typos, negative days between monitoring events, and mislabelled data flagged and resolved with field staff records.
  - Taxonomic standardization and naming consistency:
    - Local names checked and mapped to Latin names (Husson et al. 2018; APG 2016; Taxonomic Name Resolution Service).
    - Skilled botanists and reference guides used for species identification.
    - Individually numbered tags enabled precise tracking of seedlings.
  - Preprocessing aligns nursery and outplanting datasets via a line-fitting approach to standardize survival and growth metrics at two years.

- Analytical methods for standardization
  - Survival and height at two years standardized using line-fitting across mortality and growth models (linear, exponential, power-law, asymptotic, logistic).
  - Best-fit model selected by Akaike Information Criterion; models with R2 < 0.5 excluded.
  - Handling of special cases:
    - Cohorts with 0% mortality that did not change were manually set to 100% survival at two years if data allowed.
    - Negative predicted heights or heights > 10 m removed.
  - Growth rates (RGRm) calculated at two years, with non-linear model adjustments per Paine et al. (2012).
  - Precipitation data (total_precip_mm) computed from PERSIANN-CDR daily data for the relevant location.

- Usage context and references
  - Data are tied to a broader restoration ecology context and the 2023 Restoration Ecology article (Harrison et al., 2023) on cumulative seedling performance from nursery to outplanting.
  - References support data standards, growth modeling, and species identification tools used in processing the dataset.

- Data accessibility and notes for data leaders
  - Four primary data files documented with detailed column definitions and units, enabling cross-study integration.
  - Metadata emphasis: provenance, collection methods, data processing steps, and quality control are explicitly described to support data discoverability and reuse.
  - Limitations: NA entries reflect insufficient data for some predictive calculations; not all cohorts yield two-year predictions due to data constraints.