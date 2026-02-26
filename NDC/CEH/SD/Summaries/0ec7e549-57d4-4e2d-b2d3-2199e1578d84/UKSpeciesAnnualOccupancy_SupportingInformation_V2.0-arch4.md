# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- National-scale, annual occupancy estimates and trends for 5,293 UK bryophyte, lichen and invertebrate species from 1970 to 2015.
- Outputs include: 1000 posterior samples of occupancy by species-region-year, summary tables (mean occupancy, 95% credible intervals, standard deviation, rhat), and derived annual growth-rate trends.
- Regional coverage includes UK, GB, England, Scotland, Wales, and Northern Ireland, depending on input data availability.
- Data are derived from observations contributed by UK recording schemes and societies and processed through a Bayesian occupancy model to handle biases in presence-only data.

## Data inputs and standardization
- Input data: presence-only occurrence records from 29 recording schemes, supplemented by Biological Records Centre and iRecord when possible.
- Standardization criteria: exact date, 1x1 km location, records from 1970 onward, UK location, deduplication, and taxonomic validation.
- Large input scale: data from 10,750 species across 31 taxonomic groups, yielding outputs for 5,293 species.

## Modelling approach
- Occupancy modelling framework accounts for the detection process and imperfect detection biases; uses a hierarchical random-walk occupancy model with country-year effects and list-length-based detection.
- Implemented via sparta (R package) with JAGS for MCMC sampling; Bayesian estimation, with iterations varying by dataset size.
- Outputs per species-region-year include a 1000-sample posterior occupancy distribution and convergence diagnostics (Rhat).

## Outputs and data formats
- Posterior samples: 1000 occupancy samples per species per region per year, stored as separate CSV files in POSTERIOR_SAMPLES.
- Summary tables: per species, per region, per year, including mean occupancy, 95% credible intervals, standard deviation, and Rhat; stored in SUMMARY_TABLES.
- Species trends: mean annual growth rate for the largest region (UK or GB), with 95% credible intervals and precision; stored in Species_Trends.
- Dataset information: metadata on input datasets (country coverage, years, schemes, counts, visits, list-length categories) in Datasets_information.csv.
- Species name provenance: origin and inclusion notes in Species_Names.csv.
- All outputs are provided as CSV files; data availability and coverage vary by taxon and region.

## Data quality, uncertainty, and usage considerations
- Estimates carry uncertainty reflecting variable data coverage and sampling intensity; interpret trends with attention to credible intervals.
- Coverage differs by species and taxon; rove beetles begin in 1980 while others start in 1970; regional coverage (UK vs GB) varies.
- Only species with at least 50 contributing records are included in outputs; users should review record counts alongside estimates.
- Use accompanying information (Datasets_information.csv, Species_Trends.csv) to understand data range, year coverage, and sampling effort for each species.

## Tools and access
- R packages for analysis: sparta (occupancy/trend estimation) and BRCindicators (time-series indicators).
- Shiny app for visualizing occupancy and detection estimates alongside trends: speciesplotviewer (with caveat that species-level outputs are intended for multispecies indicators).
- Citations required when using data or app, linked to the associated data paper and methodological references.

## Implications for data strategy and collaboration
- Demonstrates end-to-end data workflow: from wide-scale citizen-science/scheme data collection to standardized inputs, rigorous occupancy modelling, and accessible outputs for conservation monitoring.
- Supports co-ownership of data products through transparent metadata, region- and taxon-specific reporting, and available analysis tools.
- Highlights importance of metadata richness (input datasets, year ranges, region coverage, name origins) to enable reuse, provenance tracking, and cross-network collaboration.
- Provides a scalable model for monitoring biodiversity change across large taxonomic groups and regions, aligning with data governance goals for data quality, discoverability, and use in policy and conservation planning.