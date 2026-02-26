# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

## Overview
- A dataset and supporting information describing seedling nursery and outplanting trials in a tropical peat-swamp forest.
- Aims to enable standardized assessment of seedling survival and growth from nursery to outplanting, with an emphasis on provenance, data quality, and metadata for reuse.

## Provenance and Study Context
- Location: Natural Laboratory of Peat-swamp Forest, Sebangau National Park, Central Kalimantan, Indonesia.
- Timeframe: 2009–2016 (nursery data collected Dec 2009–Feb 2014; outplanting monitoring through 2019–2020 for some trials).
- System context: Ombrogenous peat-swamp forest previously affected by logging and drainage; restoration experiments include nursery rearing and outplanting of native species under varied conditions.
- Data lineage: Associated with Harrison et al. (2023); includes detailed methods for data collection, quality control, and data processing.

## Datasets Included
- Nursery_cohort_summary.csv
  - Aggregated nursery-level data for cohorts (same species, seedling origin, and nutrient treatment entering the nursery in a given month).
  - Key metrics: survival at 2 years, final mortality, height at 2 years, relative growth rate (RGRm), precipitation, and cohort-level statistics (e.g., number planted, duration, mortality, etc.).
- Nursery_individual_tree.csv
  - Individual nursery seedling monitoring data (one row per monitoring event per tree, with tagN as unique identifier).
  - Variables include survival, height, basal diameter, number of leaves, duration, origin, nutrients, and batch information.
- Outplanting_cohort_summary.csv
  - Cohort-level summaries for outplanted seedlings, defined by project, site, transect, species, and treatment.
  - Metrics include survival at 2 years, final mortality, height at 2 years, RGRm, number planted, and timing data.
- Outplanting_individual_tree.csv
  - Individual outplanted seedling monitoring data (one row per monitoring event per tree).
  - Variables include plantingDate, monitoringDate, duration, height, diam_basal, leaves, survival, site, transect, treatment, and tagN.

## Data Collection and Methods
- Nursery data
  - Two seedling nurseries within the Sebangau research site; one embedded in forest conditions, another near the forest edge.
  - Seedlings sourced from adjacent relatively undisturbed forest; tagging ensured individual tracking.
  - Nursery treatments include fertilised, non-fertilised, or unknown; seedlings categorized as seedling-origin or wildling-origin.
  - Monitoring records include alive/dead status and height (cm), with monthly checks and occasional weekly/biweekly intervals during peak periods.
- Outplanting data
  - Six distinct trials/projects (RG-2009, RF-2012, RF-2013, DH-2014, LH-2016, BFA-2016) with diverse site conditions (open burns, forest edge, relatively undisturbed forest).
  - Planting conditions included seedlings grown in nursery or sourced as wildings; various planting treatments (e.g., bakul baskets, shade structures, combinations, or controls).
  - Monitoring intervals varied by project (monthly initially, then less frequent or annually in some trials).
  - Species, site conditions, and treatments are harmonized into cohort identifiers for cross-study analyses.

## Data Structure and Key Variables
- Four data files with clearly described fields and units (detailed in accompanying Tables 1–4 in the documentation).
- Examples of essential fields:
  - Species information: species_local (local name) and species_latin (scientific name).
  - Origin: origin (seedling vs wildling) and batch identifiers.
  - Temporal data: nursery_entry_date, planting_year/month, monitoring_date/date ranges.
  - Growth and survival: height_cm, diam_basal_cm, number_leaves, survival, duration_days, final_mortality_per_mean, height_final_mean, RGRm_mean, etc.
  - Environmental context: total_precip_mm (2-year total precipitation per site, derived from PERSIANN-CDR data).
- Data processing
  - Tree tagging, standardization to Latin names, and verification against taxonomic references (APG IV, among others).
  - Line-fitting approaches to standardize survival and height at two years across cohorts; models selected by Akaike Information Criteria with R2 thresholds; manually adjusted cases where data were insufficient.

## Quality Control and Metadata
- Observer training and ongoing refresher sessions to ensure consistent data collection across the project team.
- Central field leadership and cross-checks to minimize errors; field data sheets recorded observer names.
- Data screening for outliers, negative time differences, typographical errors, and missing data; resolved through team consultation and supplemental field reports.
- Taxonomic standardization: local names validated and converted to Latin binomials; species identification guided by established references.
- Unique tagging system (per seedling and per cohort) to enable reliable tracking of survival and growth across nursery and outplanting stages.

## Analytical Methods and Standardization
- Standardized survival and height measures at two years (730 days) using a line-fitting approach across nursery and outplanting data.
- Survival at two years (survival_per_2yrs_mean), half-life (half_life_mean), final mortality (final_mortality_per_mean): derived from linear, exponential, power-law, asymptotic, and logistic models; best fit selected using AIC and R2 > 0.5 criterion. Cases with 0% mortality and non-changing data were set to 100% survival after two years.
- Height at two years (height_cm_2yrs_mean, height_cm_2yrs_sd): derived from fitted growth trajectories; negative or implausible values filtered.
- Relative Growth Rate (RGRm_mean, RGRm_sd): calculated at two years using line-fit methods; non-linear model adjustments referenced from Paine et al. (2012).
- Total precipitation (total_precip_mm): computed per cohort location using PERSIANN-CDR data.

## Data Governance and Reuse Considerations
- Provenance preserved through linkage to Harrison et al. (2023) and explicit methodological references.
- Data are richly documented with explicit data structures, units, and processing steps to enable reuse in restoration ecology, forest rehabilitation studies, and cross-site meta-analyses.
- Limitations and caveats
  - Some cohorts have incomplete data preventing model-based predictions (marked as NA); notably, cohorts with zero observed mortality or insufficient temporal replication.
  - Variable monitoring durations and cohort sizes across projects; careful interpretation required when aggregating across trials.
  - Data are tied to specific field sites and project contexts, which may limit generalizability without harmonized metadata.

## References and Related Methods
- Methodological references for growth modeling, mortality fitting, and standardization across studies (e.g., Paine et al. 2012; Smith et al. 2022; Harrison et al. 2023) are cited within the dataset documentation.
- Precipitation data provenance via PERSIANN-CDR (Sorooshian et al. 2014; Ashouri et al. 2015) is used to contextualize growth and survival analyses.

## How to Use
- Researchers can leverage the four CSV files to analyze cohort-level survival and growth, compare nursery-to-outplanting performance, and explore the effects of site conditions and treatments on reforestation outcomes.
- The metadata and data structure documentation support integration with other datasets and replication of the standardization workflow for cross-study comparisons.