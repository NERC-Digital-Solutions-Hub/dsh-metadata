# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

- A dataset and supporting information from a study of native tree seedling nursery and outplanting performance in Sebangau National Park, Central Kalimantan, Indonesia, covering 2009–2016 and linked to Harrison et al. (2023).
- Focuses on nursery cohorts and outplanted cohorts across multiple trials to assess survival and growth for reforestation in tropical peat-swamp forest.

## Provenance and study context

- Data were collected in the Natural Laboratory of Peat-swamp Forest, Sebangau National Park, a historically logged peatland with drainage canals that increased fire risk.
- Study involves nursery propagation of 40 native species (seedlings and wildlings) and six outplanting trials using various species mixes, planting treatments, and site conditions.
- Nursery data span December 2009–February 2014; outplanting trials span 2009–2019 (monitoring extended to 2016–2020 for some trials).
- Precipitation data for seedling growth were sourced from PERSIANN-CDR (daily precipitation data for the 0.25-degree grid cell including the site).

## Datasets and schema (GIS-relevant data products)

- Four CSV data files are included:
  - Nursery_cohort_summary.csv: summary survival and growth for nursery cohorts (grouped by species, seedling origin, and nutrient treatment, entered in a given month).
  - Nursery_individual_tree.csv: per-tree nursery monitoring data (one row per monitoring event per individual seedling).
  - Outplanting_cohort_summary.csv: summary survival and growth for outplanting cohorts (grouped by project/site/transect/species/treatment).
  - Outplanting_individual_tree.csv: per-tree outplanted monitoring data (one row per monitoring event per individual seedling).
- Each file follows a detailed data schema describing fields such as species_local, species_latin, origin, nursery_entry_date, monitoring_sequence, duration_days, height_cm, diam_basal_cm, survival, nutrients, and total_precip_mm (2-year total).
- Data are organized to support cross-comparison of nursery-to-outplanting performance and standardized metrics at two years.

## Locations and geospatial aspects

- Nursery locations:
  - Nursery 1 coordinates: 2°19'00.46"S, 113°54'28.23"E (established 2005).
  - Nursery 2 coordinates: 2°18'58.56"S, 113°54'29.40"E (established 2010).
- Outplanting trials cover six projects with explicit planting start dates and site characteristics (e.g., Open old burn, Open recent burn, Forest edge, Relatively undisturbed forest).
- Trials include multiple transects/plots per project, with site-specific distances from forest edge, flooding risk, planting densities, and seedling sources (seed/wilding).
- Precipitation data used for 2-year growth/survival assessments are tied to the 0.25-degree grid cell around the study location (PERSIANN-CDR).

## Data collection methods and treatment details

- Seedling sources:
  - Seedlings grown from seed (seedling) or wildlings collected in nearby forest (wildling).
- Nursery conditions:
  - Two nurseries with shading nets to reduce insect damage and provide 50% shading; exposed to natural rainfall.
- Outplanting trials:
  - Six distinct trials with varying species mixes (up to 24 species across trials), planting in nursery-derived seedlings, with or without treatments such as bakul (weaved organic baskets), roof shading, or combinations.
  - No root pruning; plastic bags removed at outplanting; some sites used bakul with or without shade, others had no treatment.
  - Monitoring schedules ranged from weekly to annual, across a total of 156 outplanted seedling cohorts and 24 planted plots/plots-equivalents.
- Site descriptors:
  - Planting site conditions include open old burn, open recent burn, forest edge, and relatively undisturbed forest.
  - Distances from forest edge and flood regimes documented per project.

## Data structure and key fields (usage guidance for GIS)

- Nursery_cohort_summary.csv: cohort-level summary metrics including
  - species_local and species_latin
  - nursery_entry_year/month
  - origin (seedling or wildling)
  - nutrients (fertilised, non-fertilised, unknown)
  - final_duration_days_mean, survival_per_2yrs_mean, final_mortality_per_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean/RGRm_sd, total_precip_mm, etc.
- Nursery_individual_tree.csv: individual seedling monitoring records
  - tagN, origin, species_local, species_latin, nursery_entry_date, duration_days, height_cm, diam_basal_cm, number_leaves, survival, batch_final, nutrients.
- Outplanting_cohort_summary.csv: cohort-level summaries for outplants
  - project, site, transect, site_broadcategory, species_local, species_latin, planting_treatment, planting_year/month, final_duration_days_mean, survival_per_2yrs_mean, number_planted, final_mortality_per_mean, half_life_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean/RGRm_sd, height0_mean, total_precip_mm.
- Outplanting_individual_tree.csv: individual outplanted monitoring records
  - project, site, transect, tagN, species_local, species_latin, planting_treatment, planting_date, monitoring_date, duration_days, duration_months, survival, height_cm, number_leaves, diam_basal_cm.

- Units and field definitions follow detailed tables in the data documentation (Tables 1–4 in the Data Structure section).

## Analytical methods and standardization (GIS relevance)

- A line-fitting approach standardizes survival and height growth to two years (730 days) across nursery and outplanting datasets.
- Metrics standardized to two years include:
  - Survival at two years (survival_per_2yrs_mean) derived from multiple mortality models (linear, exponential, power, asymptotic, logistic) with model selection by AIC and R2 > 0.5; cohorts with 0% mortality and non-changing data are set to 100% survival if monitoring exceeded two years.
  - Height at two years (height_cm_2yrs_mean and height_cm_2yrs_sd) derived from height-time fits; negative or >10 m predictions are removed.
  - Relative growth rate (RGRm_mean and RGRm_sd) at two years, with adjustments for non-linear models as per referenced methods.
- Total precipitation (total_precip_mm) over two years is computed from daily precipitation data (PERSIANN-CDR) for site location.

## Quality control, data standards, and curation

- Team training and field leadership ensured consistent data collection; Salahuddin served as field team leader.
- Data screening for outliers, negative days between monitoring, typos, and missing values; corrections made with field notes and ongoing monthly activity logs.
- Consistency in species naming: local names validated and converted to Latin names using taxonomic references (APG IV, Husson et al. 2018, etc.); local botanists used for species identification.
- Individual seedlings tracked with unique tags to ensure reliable survival and growth records.

## Practical notes for GIS specialists

- The dataset offers rich spatial-temporal information: precise nursery locations, multiple transects/plots, and site categories that enable spatial analyses of survival and growth across gradients (burn history, edge effects, and undisturbed forests).
- Includes standardized two-year metrics suitable for comparative mapping and cross-project GIS analyses.
- Precipitation data linked to site coordinates supports environmental covariate analyses (e.g., rainfall-driven growth/survival).
- Data quality and tagging enable lineage tracking (seedling-to-outplanting) for spatial performance studies.

## Limitations and caveats

- Some entries contain NA values for certain metrics (e.g., survival at two years or assay-specific metrics) where data were insufficient to fit predictive models.
- Line-fitting could not be applied to cohorts with static or 0% mortality; such cases are handled manually as noted.
- Data cover multiple projects with differing monitoring intervals; standardized two-year metrics address duration differences but some longitudinal nuances remain project-specific.

## References (selected)

- Angiosperm Phylogeny Group (2016)
- Ashouri et al. (2015) on PERSIANN-CDR
- Boyle et al. (2013) Taxonomic Name Resolution Service
- Graham et al. (2007) tropical peat swamp forest growth strategies
- Harrison et al. (2023) Accounting for cumulative seedling performance from nursery to outplanting
- Paine et al. (2012) nonlinear plant growth modeling
- Sorooshian et al. (2014) PERSIANN-CDR data
- Thomas (2013) Field guide for tree species identification