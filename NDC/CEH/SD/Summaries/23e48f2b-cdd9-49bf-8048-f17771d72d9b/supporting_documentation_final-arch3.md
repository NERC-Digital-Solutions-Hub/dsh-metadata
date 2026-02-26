# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

## Aim and scope (relevance to monitoring frameworks)
- Provides standardized, cross-study measures of seedling performance to evaluate reforestation efforts from nursery to outplanting.
- Data support scrutinizing restoration outcomes and informing future monitoring design across nursery and field deployment.
- Four integrated data files capture cohort- and individual-level survival and growth across multiple trials and site conditions.

## Provenance and study context
- Data collected in the Natural Laboratory of Peat-swamp Forest special research zone, Sebangau National Park, Central Kalimantan.
- Historical disturbances include selective logging (until 1997) and illegal hand-logging (until 2004), leading to peat drainage and fire risk; seedlings were planted to test restoration performance.
- Two nurseries (2005 and 2010) replicated forest and edge conditions; six small-scale outplanting trials tested native species under varied site conditions and treatments.
- Precipitation data derived from PERSIANN-CDR to align with survival and growth calculations.

## Study design and treatments
- Nursery phase: 40 native peat-swamp forest species from 29 genera; seeds collected from adjacent forest; seedlings monitored for alive/dead status and height (cm) with tagging for tracking.
- Outplanting phase: six projects with diverse conditions (open old burn, open recent burn, forest edge, relatively undisturbed forest) and treatments, including seedling vs wilding sources, and various post-planting management (e.g., bakul baskets, shading roofs, combinations, or controls).
- Planting details include coordinates, burn history, distance to forest edge, flood regime, planting density, and weed management (or lack thereof).

## Data collection and data sources
- Nursery data: monitoring of seedling cohorts entered monthly, with cohort-level attributes (species, origin, fertilization status, monitoring duration, survival, growth metrics, and total precipitation exposure).
- Outplanting data: monitoring at multiple intervals (monthly to yearly, depending on project) for individual seedlings and cohort summaries; includes survival, height, basal diameter, leaves, and treatment details.
- Site and climatic context: detailed site characteristics for each project; precipitation data used to compute total 2-year rainfall per cohort.

## Data structure and files (key contents)
- Nursery_cohort_summary.csv
  - Summary survival and growth for nursery cohorts (grouped by species, origin, nutrient treatment, entry month/year).
  - Variables include final duration, 2-year survival, final mortality, height at 2 years, growth rates, and total precipitation.
- Nursery_individual_tree.csv
  - Individual nursery tree monitoring data (one row per monitoring event per seedling), including tag, origin, species, nursery date, duration, height, basal diameter, leaves, survival, and treatment.
- Outplanting_cohort_summary.csv
  - Summary survival and growth for outplanting cohorts (project, site, transect, species, treatment, planting year/month).
  - Variables include final duration, 2-year survival, final mortality, height at 2 years, RGR, number planted, site characteristics, and total precipitation.
- Outplanting_individual_tree.csv
  - Individual outplanted tree monitoring data (one row per monitoring event per seedling), including project, site, transect, tag, species, planting and monitoring dates, duration, height, leaves, survival, and treatment.

## Analytical methods and standardization (monitoring metrics)
- Standardization approach: line-fitting to derive comparable two-year metrics across nursery and outplanting data.
- Outcome metrics (two-year standardizations):
  - Survival at two years (survival_per_2yrs_mean): predicted from linear, exponential, power-law, asymptotic, and logistic models; model with lowest AIC selected; require R2 ≥ 0.5; cohorts with 0% mortality not changing over time are manually set to 100% survival if duration > two years.
  - Height at two years (height_cm_2yrs_mean, height_cm_2yrs_sd): similarly modeled; negative predictions removed; unrealistic heights (>10 m) excluded.
  - Relative growth rate (RGRm_mean, RGRm_sd): computed at two years using line-fitting; for nonlinear models, adjusted per Paine et al. (2012).
- Precipitation context: total 2-year precipitation (total_precip_mm) derived from PERSIANN-CDR data for each cohort’s location.
- Data processing and references: methodology described in Analytical Methods; line-fitting approach aligns with Smith et al. (2022) and Harrison et al. (2023).

## Quality control, metadata, and data governance
- Observer training and ongoing refresher training; field team leadership ensured consistency.
- Data verification: screening for outliers, data entry errors, typos, and missing data; corrections with field records and team input; field team members recorded for traceability.
- Species identification and nomenclature standardized using established taxonomic references (Husson et al. 2018; Angiosperm Phylogeny Group 2016; Taxonomic Name Resolution Service).
- Individual seedling tagging and consistent identification across nursery and outplanting to support reliable survival and growth tracking.

## Reproducibility and data use considerations for monitoring frameworks
- Four clearly defined data files with comprehensive variable dictionaries and units (Tables 1–4 in the data structure) to enable reproducibility and cross-study comparisons.
- Use of accessible models and criteria (AIC, R2 thresholds) to determine standardized outcomes; transparent handling of special cases (e.g., 0% mortality not changing).
- Open data practices necessitated by data sharing constraints are acknowledged, with explicit note on the need for metadata and dataset provenance.

## Contextual references and provenance
- Core sources include Harrison et al. (2023) for the overarching framework and interpretation; Smith et al. (2022) for line-fitting standardization approach; supporting methodological references for growth models and taxonomic standards.
- Precipitation data and environmental context drawn from PERSIANN-CDR (Sorooshian et al. 2014; Ashouri et al. 2015) and related methodological guidance.