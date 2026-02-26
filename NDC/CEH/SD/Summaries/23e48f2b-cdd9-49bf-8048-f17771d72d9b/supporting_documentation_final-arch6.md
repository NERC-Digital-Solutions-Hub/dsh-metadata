# Sebangau National Park, Central Kalimantan, Indonesia, 2009-2016

- A Supporting Information package for Harrison et al. (2023) detailing data from nursery and outplanting trials in Sebangau National Park, with associated datasets and methods.
- Aim: document provenance, collection, processing, and standardization of seedling survival and growth data to support reforestation on degraded tropical peatlands.

## Data provenance and context

- Collected in the Natural Laboratory of Peat-swamp Forest (Sebangau), Central Kalimantan, Indonesia.
- Background: historical logging and peat drainage, with subsequent trials of tree planting to test native species performance under varying conditions.
- Data cover nursery seedling cohorts and outplanted seedlings across six small-scale trials (projects RG-2009, RF-2012, RF-2013, DH-2014, LH-2016, BFA-2016) from 2009–2019, with two nurseries and long-term monitoring.
- Precipitation data used for context: daily PERSIANN-CDR data matched to site for two-year total rainfall.

## Datasets included

- Nursery_cohort_summary.csv
  - Summary survival and growth for nursery cohorts (grouped by species, seedling origin, and nutrient treatment) entering the nursery each month.
  - Key metrics: survival at 2 years, final mortality, height at 2 years (with SD), relative growth rate (RGRm), cohort size, 2-year precipitation totals, and line-fit derived estimates.
- Nursery_individual_tree.csv
  - Individual nursery monitoring records for each seedling (one row per monitoring event per seedling).
  - Variables include tag number, origin, species, nursery entry date, duration, height, basal diameter, leaves, survival, fertilization status, and batch identifier.
- Outplanting_cohort_summary.csv
  - Summary survival and growth for outplanting cohorts (defined by project, site, transect, species, and treatment).
  - Key metrics: 2-year survival, final mortality, height at 2 years (with SD), RGRm, number planted, monitoring duration, and total precipitation.
- Outplanting_individual_tree.csv
  - Individual outplanted seedling monitoring records (one row per monitoring event per seedling).
  - Variables include project, site, transect, tag, species, planting treatment, planting date, monitoring date, duration, height, leaves, survival, and diameter.

## Data collection and quality control

- Nursery data: two nurseries (2005 and 2010 constructions) with shaded netting to reduce herbivory; seedlings tracked with unique tags; seeds from adjacent undisturbed forest; fertilization status recorded.
- Outplanting trials: six distinct trials with varying site conditions (open old burns, open recent burns, forest edge, relatively undisturbed forest), seedling sources (seed/wilding), and treatments (e.g., bakul, roof, bakul + roof, controls).
- Monitoring: standardized measurement of survival, height, and other growth metrics over multi-year periods.
- Quality control: rigorous observer training, field leader oversight, duplicate checks against monthly field reports, outlier screening, correction of typos, consistent local-to-Latin species naming (APG/Husson et al.), and use of unique tags for traceability.

## Data structure and key variables

- Four CSV files structured with detailed metadata tables (Tables 1–4 in the data documentation).
- Common themes across files:
  - Species information: local and Latin names, origin (seedling vs wildling).
  - Monitoring timelines: entry dates, monitoring dates, durations (days/months).
  - Growth and survival metrics: height (cm), basal diameter (cm), number of leaves, survival status (alive/dead), mortality percentages, and derived growth metrics.
  - Treatments and site context: fertilization status, nursery treatments, planting treatments (e.g., bakul, roof), site conditions, and transects.
  - Environmental context: total precipitation over the relevant period (from PERSIANN-CDR data).
- Analytical-ready fields include line-fitted, standardized metrics such as survival_per_2yrs_mean, height_cm_2yrs_mean, height_cm_2yrs_sd, RGRm_mean, final_mortality_per_mean, half_life_mean, and total_precip_mm.

## Analytical methods and standardization

- Standardization approach: line-fitting of mortality and growth over time to standardize to two-year benchmarks (730 days) across nursery and outplanting cohorts.
- Derived metrics:
  - Survival at two years (survival_per_2yrs_mean): best-fitting model selected by lowest AIC; models with R^2 < 0.5 excluded; 0% mortality cohorts with no change manually assigned as 100% survival if monitoring exceeded two years.
  - Height at two years (height_cm_2yrs_mean, height_cm_2yrs_sd): similarly fitted; negative predictions or >10 m removed.
  - Relative growth rate (RGRm_mean, RGRm_sd): calculated at two years; adjustments for non-linear models per Paine et al. (2012).
- Data processing and naming follow Harrison et al. (2023) and adherence to standardized formatting for reproducibility.

## Data usage notes

- The dataset enables cross-study comparisons of nursery and outplanting performance for multiple native peat-swamp species under varied conditions.
- Derived metrics allow assessment of early-stage performance and potential predictors of survival and growth, suitable for informing restoration strategies.
- Comprehensive quality control and provenance details support reproducibility and re-use in meta-analyses or re-analysis with updated models.

## References (context for data methods)

- APG IV classification (Angiosperm Phylogeny Group, 2016)
- PERSIANN-CDR precipitation data (Ashouri et al., 2015; Sorooshian et al., 2014)
- Taxonomic name resolution and field guides (Boyle et al., 2013; Thomas, 2013)
- Methods for nonlinear growth modeling and growth rate calculations (Paine et al., 2012; Smith et al., 2022)
- Restoration ecology study linking seedling performance to reforestation outcomes (Harrison et al., 2023)
- Related datasets and context (Graham et al., 2007; Husson et al., 2018)