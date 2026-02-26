# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Overview
- Provides annual abundance indices and trends for 477 moth species (mostly macro-moths) from 1968–2021 across Britain, Ireland, and the Channel Islands.
- Uses a Generalized Abundance Index (GAI) model to produce:
  - Abundance indices (per year) with 95% bootstrap confidence limits
  - Temporal trends: Annual Growth Rate (AGR) and total percentage change over the time series
- Includes both whole-network results and country-level analyses for England, Scotland, and Wales.
- Outputs are delivered as region-wide datasets with explicit uncertainty measures.

## Data source and network context
- Based on the Rothamsted Insect Survey (RIS) light-trap network, one of the longest-standardised terrestrial insect time series.
- Light-traps sample locally (approximately 60 active traps currently; historically around 560 locations; average ~90 traps/year) with a 400–700 nm tungsten bulb.
- Traps are near power sources and human-maintained sites, sampling local nocturnal moth communities.
- RIS data have supported numerous ecological and climate-related studies and are publicly linked via the Rothamsted Insect Survey online data warehouse.

## Data used and processing
- Counts: 4,934,822 abundance counts across 844 species (1968–2021) from all traps in Britain & Ireland (551 traps, average ~92/year).
- Taxa: predominantly macro-moths; a small number of easily identified micro-moth species retained for consistency (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis). Some species time periods were shortened due to taxonomic/data issues.
- Aggregation: some taxa were analyzed as species aggregates due to taxonomic changes or identification issues.
- Time period adjustments: several species had reduced time spans (see Notes on time periods in the dataset).

## Analytical method (GAI)
- Stage 1: Generalized Additive Model (GAM) to estimate annual abundance curves per species, standardised so area under the curve equals one (per-site curves used to correct within-year gaps).
- Stage 2: Poisson GAMs to derive site- and year-specific abundance indices; scaling up to the network assumes typical trap conditions and weekly monitoring.
- Trends: year term modeled as continuous to estimate linear trends; AGR computed as exp(year coefficient) − 1; perc_cng derived from AGR over the number of years.
- Uncertainty: 95% CIs obtained via bootstrapping (1,000 replicates) for indices and trends.

## Dataset description and structure
- Output format: two CSV files per region
  - Indices: suffix _indices
  - Trends: suffix _trends
- Region prefixes:
  - bi_ for Britain, Ireland, and Channel Islands
  - eng_ for England
  - scot_ for Scotland
  - wales_ for Wales
- Abundance index file columns:
  - species, name, common_name, year, nsites, nsites_pos, index, index_low, index_upp, nboot
- Trend file columns:
  - species, name, common_name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year
- Supplementary lookup: supplementary_spp_names.csv
  - Maps Rothamsted species IDs to external taxonomic codes and names (BRC, UKSI/Agassiz et al. checklists, Bradley & Fletcher IDs)
  - Columns include species_id, brc_concept, brc_species_name, abh_code, abh_species_name, abh_common_name, bf_code, england, scotland, wales

## Data quality, coverage, and accessibility
- Quality criteria applied to determine which species meet analysis reliability; results: 477 species for Britain & Ireland; 441 England; 242 Scotland; 232 Wales.
- Coverage: broad geographic scope with country-level and regional breakdowns; data quality checks consider data completeness and confidence interval width.
- Access: data available via the Rothamsted Insect Survey online data warehouse; full dataset described here is provided as CSV files with clear naming conventions.

## How this supports data use and products
- Enables self-serve exploration of long-term moth abundance and trends across regions, with clear uncertainty (CIs).
- Facilitates cross-regional comparisons (Britain & Ireland vs. England/Scotland/Wales) and temporal trend analysis.
- The supplementary names file aids data integration with external datasets and taxonomic lookups.
- Suitable for dashboards, pivot analyses, or scripted pipelines to monitor biodiversity indicators and detect long-term changes in moth populations.

## Acknowledgements and references
- Funding: Defra (Outcome Indicator Framework Wildlife Indicator Development, C13638); RIS funded by BBSRC; UK-SCAPE National Capability (NERC NE/R016429/1).
- References include foundational work on the GAI method and long-term monitoring of moths, climate impacts, and biodiversity trends.