# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## Purpose and what the dataset provides for monitoring
- Provides long-term environmental health indicators for moths across Britain and Ireland, with country-level results for England, Scotland, and Wales.
- Outputs include annual abundance indices and trends (177? actually 477 species) derived from a robust statistical framework to support policy scrutiny, evaluation, and future decision-making.
- Trends are presented as Annual Growth Rate (AGR) and total percentage change over the time series, both with 95% bootstrapped confidence intervals.

## Data scope and time period
- Data from the Rothamsted Insect Survey light-trap network, covering 1968–2021.
- 477 species (mostly macro-moths) analyzed for Britain and Ireland; 441 (England), 242 (Scotland), and 232 (Wales) meet quality criteria for regional analyses.
- Data encompass 4,934,822 abundance counts from 551 traps (average ~92 traps/year) across Britain & Ireland; a large, long-running invertebrate time series.

## Methodology (GAI framework)
- Generalized Abundance Index (GAI) approach:
  - Stage 1: Generalized Additive Models (GAMs) to estimate species-specific annual abundance curves, standardized so area under the curve equals one; produce site-level indices correcting for within-year recording gaps.
  - Stage 2: Poisson GAMs with site and year as explanatory variables to estimate indices and trends; convert year effects into an AGR (exponentiated year coefficient minus 1) and compute total percentage change.
- Temporal trends derived from a continuous-year model; bootstrapping (1,000 replicates) provides 95% confidence intervals for indices and trends.
- Quality assessment criteria determine which species’ results are reported, ensuring sufficient data across the time series and halves of the period.

## Outputs and data products
- Two main result files per region:
  - Indices: annual abundance indices for each species, with confidence intervals, plus metadata per year.
  - Trends: AGR and total percentage change with confidence intervals, plus metadata on data coverage.
- Regional groupings:
  - Britain, Ireland, and Channel Islands (bi_ prefix)
  - England (eng_ prefix)
  - Scotland (scot_ prefix)
  - Wales (wales_ prefix

## Data structure and key columns
- Indices files contain:
  - species, name, common_name, year, nsites, nsites_pos, index, index_low, index_upp, nboot
- Trends files contain:
  - species, name, common_name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year
- Supplementary taxonomic names/files:
  - supplementary_spp_names.csv maps Rothamsted IDs to BRC, UKSI (via Agassiz et al. checklist), and Bradley & Fletcher IDs.
  - Columns include species_id, brc_concept, brc_species_name, abh_code, abh_species_name, abh_common_name, bf_code, bi, england/scotland/wales indicators.

## Data access and usage
- Data are provided as CSV files; accessible via the Rothamsted Insect Survey online data warehouse (data and description available at insectdatabase.rothamsted.ac.uk).
- Supplementary names lookup aids cross-referencing with external datasets for policy-relevant analyses.

## Relevance for monitoring frameworks and governance
- Delivers standardized, long-term indicators of insect (moth) abundance and trends suitable for monitoring environmental health and evaluating policy impacts over decadal scales.
- Transparent methodology (GAI, bootstrapped CIs) supports reproducibility, auditability, and comparability across regions and time.
- The country-level breakdown enables region-specific policymaking and targeted conservation assessments.
- Data governance considerations embedded in the dataset design (clear metadata fields; explicit data availability; potential burden of data sharing and transformation).

## Data quality, limitations, and governance considerations
- Strengths:
  - Long-running, standardized time series with robust statistical treatment and quantified uncertainty.
  - Large sample size across numerous traps and species enhances reliability for broad monitoring conclusions.
- Limitations and barriers for monitoring use:
  - Occurrence of data gaps and variable data richness across species and years, leading to quality-based inclusion criteria.
  - Taxonomic issues necessitating occasional aggregation (species groups) or time-period adjustments for certain taxa.
  - Geographic coverage is strong in England, Scotland, Wales, and parts of Ireland, but Ireland has relatively limited coverage; spatial biases may affect network-wide inferences.
  - Data are tied to local light-trap sampling, which primarily captures local fauna and may be influenced by habitat context and proximity to human activity.
  - Public sharing of underlying data can be a barrier in some cases; the dataset explicitly provides indices/trends with associated metadata to mitigate this.
- Practical considerations for governance:
  - Ensure metadata completeness and clarity when integrating with other datasets (the supplementary names file helps with cross-dataset matching).
  - Be mindful of potential changes in trap availability over time when interpreting long-term trends.

## Summary of utility for policy, monitoring and future decisions
- Enables evidence-based assessment of long-term moth population changes and potential climate- or habitat-change signals.
- Supports monitoring of biodiversity baselines, trend detection, and evaluation of conservation/intervention outcomes.
- Provides a replicable framework (GAI) for future monitoring programs, including data handling, model structure, and uncertainty quantification.
- Facilitates transparent reporting to stakeholders through standardized indices, trends, and confidence intervals.