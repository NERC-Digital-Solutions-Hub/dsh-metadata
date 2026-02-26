# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

## Scope and purpose
- Provides abundance trends for 432 moth species (mostly macro-moths) from the Rothamsted Insect Survey (RIS) light-trap network, covering 1968–2016.
- Presents trends as year coefficients (Annual Growth Rate, AGR) and total percentage changes over the time series, with 95% and 90% confidence intervals.
- Two trend datasets are provided:
  - BI: Britain & Ireland, 1968–2016 (all traps)
  - GB: Great Britain, 1970–2016 (GB-only subset)
- Data supports long-term monitoring and analysis of population changes, with explicit notes on data reliability and coverage.

## Background and data sources
- RIS operates two trap networks (aphids and moths) running since the 1960s; light-traps sample local moth fauna with emphasis on nearby, not long-distance, dispersal.
- The light-trap network has around 80 active traps currently; historically more than 600 locations with typical annual operation of ~100 traps.
- The dataset is built from over 14 million individual moth captures from more than 1,500 species, contributing to wide-ranging scientific work on diversity, climate effects, and population trends.

## Data and sample sizes
- Analytical dataset: 4,687,310 abundance counts across 766 species (541 traps in Britain & Ireland; average ~95 traps per year).
- Predominantly macro-moths; a small number of easily identified micro-moths also included (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis).
- Analyses largely at species level; some taxa are aggregated due to taxonomic or identification issues.
- GB analyses cover 430 reliable species; BI analyses cover 432 reliable species.
- Some species have altered time ranges due to data issues or taxonomic identification changes (examples listed in the dataset).

## Analytical method (GAI)
- Uses Generalized Abundance Index (GAI) to handle seasonal patterns in count data.
- Steps:
  - Generalized Additive Model to estimate annual flight curves for each species; curves are standardized to unit area.
  - Corrects within-year recording gaps to produce site-specific annual abundance indices.
  - Poisson regression with site (categorical) and year (continuous) to estimate temporal trends.
- Outputs:
  - Year coefficient from Poisson model (baseline trend)
  - AGR: exponential of the year coefficient minus 1 (annual growth rate)
  - Total percentage change across the time series
  - Bootstrapped confidence intervals (1,000 replicates) for indices and trends (95% and 90% levels)

## Dataset structure and fields
- Provided as a comma-separated text file (CSV).
- Two main result sets distinguished by column prefixes:
  - BI_… columns for Britain & Ireland (1968–2016)
  - GB_… columns for Great Britain (1970–2016)
- Key columns include:
  - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
  - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR
  - BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP
  - BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
  - BI_AGR, BI_AGR_LOW, BI_AGR_UPP
  - BI_AGR_90LOW, BI_AGR_90UPP
  - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP
  - BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
  - GB equivalents for the GB subset (GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, etc.)
- Supplementary lookup file: moth_names_codes_lookup.csv
  - Links SPECIES_ID to BRC_CONCEPT, BRC_SPECIES_NAME, ABH_NUMBER, ABH_NAME, BF_NUMBER
  - Facilitates crosswalk to external taxonomic codes and checklists (BRC, UKSI, Agassiz et al. checklist)

## Data quality, reliability, and limitations
- Reliability: 432 BI species and 430 GB species deemed reliable for trend interpretation (expert-judged based on underlying data and model results).
- Some species have restricted time periods due to taxonomic or data issues (noted in table of exceptions).
- Taxonomic and identification inconsistencies in earlier years led to selective time periods for certain groups (e.g., Eupithecia pug species).
- Light-trap sampling is inherently localized (atmospheric conditions, moon phase, weather) and reflects local population dynamics rather than continental-scale trends.
- Trends depend on adequate trap coverage and consistent identification over time; metadata and quality checks accompany the release.

## Access, format, and discoverability
- Data provided as CSV with clearly labeled BI and GB columns for dual analyses.
- Metadata includes data sources, methods, and limitations to support proper interpretation and reuse.
- Supplementary taxonomic mapping file aids data integration with external biodiversity resources.

## Usage and applications for data leadership
- Long-term biodiversity monitoring and policy relevance: informs ecological risk assessments, climate impact studies, and conservation planning.
- Data governance opportunities:
  - Emphasizes clear provenance and methodological documentation (GAI, bootstrapping).
  - Highlights need for consistent taxonomic standards and handling of time-period gaps.
  - Demonstrates the value of dual-scope datasets (BI and GB) for cross-network comparability.
- Potential for integration with other datasets to enhance system-wide data discovery, interoperability, and actionable insights.

## Acknowledgements and references
- Funded by NERC and BBSRC under ASSIST and related programmes; RIS funded as a National Capability.
- References include foundational papers on GAI, long-term moth population studies, and biodiversity indicators, with numerous studies cited across taxonomy, climate effects, and population trends.