# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Overview
- Provides annual abundance indices and trends for 477 moth species (mostly macro-moths) sampled by the Rothamsted Insect Survey (RIS) light-trap network from 1968 to 2021.
- Trends are expressed as year coefficients from a Generalized Abundance Index (GAI) model, reported as Annual Growth Rates (AGR) and total percentage change over the time series, with 95% confidence intervals via bootstrapping.
- Indices and trends are available for the entire network across Britain, Ireland, and the Channel Islands, plus country-level analyses for England, Scotland, and Wales.

## Data source and sampling framework
- Data come from the RIS light-trap network, part of two long-running insect sampling networks (light-traps and suction traps) that have operated since 1964.
- Light-traps sample local moth communities with a standard design (200W tungsten bulb, trap height 1.2 m, opaque lid) and a narrow attraction radius, focusing on local fauna.
- Current network: around 60 active traps; historically up to ~560 locations with an average of ~90 traps operating annually. Traps are distributed to cover England, Scotland, Wales, Channel Islands; Ireland has comparatively less coverage.
- Data volume: more than 14 million individual moths captured and identified across >1,500 species. The dataset used for the analyses comprises 4,934,822 abundance counts across 844 species (primarily macro-moths), spanning 1968–2021.

## Data structure and formats
- Provided as comma-separated text files (CSV) in region-specific sets:
  - Two result files per region: one with annual abundance indices (_indices) and one with abundance trends (_trends).
  - Regional prefixes: bi_ (Britain, Ireland & Channel Islands), eng_ (England), scot_ (Scotland), wales_ (Wales).
- Columns in abundance indices (_indices):
  - species, name, common_name, year, nsites, nsites_pos, index, index_low, index_upp, nboot
- Columns in trends (_trends):
  - species, name, common_name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year
- Supplementary names lookup: supplementary_spp_names.csv, linking Rothamsted IDs to external taxon codes and checklists (BRC, UKSI, Agassiz et al., Bradley & Fletcher).
  - Columns include: species_id, brc_concept, brc_species_name, abh_code, abh_species_name, abh_common_name, bf_code, bi, england, scotland, wales
- Notes on data curation:
  - Most analyses cover 1968–2021; for some species, shorter periods are used due to taxonomic or data issues (e.g., Eupithecia spp., others listed in tables).

## Analytical method and interpretation
- Method: Generalized Abundance Index (GAI) with two-stage modeling.
  - Stage 1: Generalized Additive Model (GAM) to estimate annual abundance curves per species, standardised to unit area under the curve to correct within-year recording gaps.
  - Stage 2: Poisson GAMs to estimate site- and year-specific indices and trends; scaling up to the network assumes typical traps and consistent monitoring.
- Indices are derived from model coefficients; regional indices scale to the number of distinct sites.
- Temporal trends are derived from a continuous-year GAM term, giving:
  - AGR: Annual Growth Rate (exponentiated year coefficient minus 1).
  - perc_cng: total percentage change over the time series.
- Uncertainty: 95% confidence intervals via bootstrapping (1,000 replicates).
- Quality criteria: species included only if indices meet predefined data quality (data completeness, confidence intervals, etc.). Britain and Ireland analyses include 477 species; England 441, Scotland 242, Wales 232.

## Dataset contents and usage notes
- Scope: Britain, Ireland, and Channel Islands; country-level results for England, Scotland, and Wales.
- Data availability: in the Rothamsted online data warehouse (insectdatabase.rothamsted.ac.uk/login); dataset is intended for long-term biodiversity assessment and related research.
- Taxonomic considerations: majority of data are macro-moths; some micro-moth species are included when consistently identified; several taxa are analyzed as aggregates due to taxonomic changes or identification issues.
- Important caveats for users:
  - Some species have reduced time periods due to taxonomic or data issues (detailed in the dataset).
  - Light-trap sampling remains a local-sample proxy; interpretation should consider trap radius, local habitat, and maintenance-related biases.
  - Trap coverage and data availability vary by region; Ireland has comparatively limited coverage.
  - Results are model-based estimates with inherent sampling and modeling uncertainty.

## Data access and governance considerations
- Data are linked to a long-running, institutional program with formal acknowledgments and funding; includes metadata describing collection methods, analytical approach, and quality filters.
- Supplementary names mapping facilitates integration with external taxonomic resources (BRC, UKSI, Agassiz et al., Bradley & Fletcher).
- For governance and reuse:
  - Ensure proper attribution to RIS, the contributing institutions, and funders.
  - Maintain traceability of taxonomic names and any updates to checklists; document any changes in time ranges due to taxonomic revisions.
  - If aggregations are used, be explicit about which taxa are included in each aggregate and the rationale.
  - When updating with new years, preserve compatibility of existing _indices and _trends formats and column definitions.

## Practical considerations for data stewards
- Standardization and interoperability:
  - Maintain consistent taxon identifiers and mappings with external checklists (UKSI, BRC, Agassiz et al., BF codes).
  - Document any taxonomic changes or reclassifications affecting time series.
- Data quality and provenance:
  - Track data completeness, proportion of years with data per species, and bootstrap counts per index/trend.
  - Preserve both raw counts and model-derived indices to support reanalysis or alternative modeling approaches.
- Distribution and updates:
  - Plan for incremental updates as new years become available and as taxonomic harmonization progresses.
  - Provide clear documentation on interpretation of indices and AGRs for non-specialist data users.

## Acknowledgements
- Analyses funded by Defra, Rothamsted Insect Survey, and associated research programs; builds on methodological developments from prior projects and publications.

## References (selected topics)
- Foundations of the GAI method and related ecological time-series analyses.
- Taxonomic checklists and moth biodiversity literature used to underpin data interpretation and supplementary naming.