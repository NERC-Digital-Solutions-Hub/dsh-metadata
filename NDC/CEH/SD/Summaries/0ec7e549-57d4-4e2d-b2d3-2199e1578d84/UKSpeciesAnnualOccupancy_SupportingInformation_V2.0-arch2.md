# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- National-scale, annual estimates of occupancy and trends for 5,293 UK invertebrate, bryophyte and lichen species from 1970 to 2015.
- Outputs include occupancy per year and region, and derived annual growth rate trends.
- Data generated from presence-only records using a Bayesian occupancy model, enabling correction for detection and sampling biases.
- Outputs provided in three forms: posterior samples, summary tables, and derived species trends.
- Regions covered: UK, GB, England, Scotland, Wales, Northern Ireland (where data permit).
- Data and methods are designed for monitoring environmental health and policy performance over time.

## Data Coverage and Input Data
- Input data: presence-only records from UK recording schemes and societies (31 groups; ~10,750 species over 29 schemes), supplemented by Biological Records Centre and iRecord.
- Total input: 22,684,449 records from 29 schemes; information includes number of records, species, sites, and visits.
- Species inclusion criteria: only species with at least 50 observations included in outputs.
- Regions and years: occupancy estimates produced for UK, GB, England, Scotland, Wales, Northern Ireland; years range from 1970 (1980 for rove beetles) to 2015.
- Data standardization: records must have exact date, 1x1 km precision, and UK location; names checked with scheme organizers; duplicates removed.

## Methods
- Modelling approach: hierarchical occupancy model with state (true occupancy) and observation (detection) components to account for imperfect detection and sampling biases.
- Data structure: detection histories with a row per site/date and a column per species; 1 indicates detection, 0 nondetection.
- Framework: random-walk occupancy model with country-year effects in the state model and list-length categorization in the detection model.
- Implementation: fitted per species with the occDetFunc function in the sparta R package (Bayesian via JAGS).
- Time span: models run from the starting year of input data (1970 or 1980) to 2015; some runs extend beyond data range for aggregation purposes.
- Run details: smaller datasets -> 40,000 iterations (burn-in 20,000, thinning 3); larger datasets -> 20,000 iterations (burn-in 10,000, thinning 3).

## Outputs and Data Format
- Posterior samples: 1000 samples from the posterior distribution of occupancy per region per species per year; stored as separate CSV files in POSTERIOR_SAMPLES (one file per species).
  - File naming example: AnnualSpeciesOccupancy_PosteriorSamples_Ants_Formica_aquilonia.csv
  - Structure: rows = 1000 x number of regions; columns include year entries (1970–2015) plus metadata (group, species, region, iteration).
- Summary tables: occupancy statistics per region-year per species; stored in SUMMARY_TABLES (one file per species).
  - File naming example: AnnualSpeciesOccupancy_SummaryTables_Ants_Formica_aquilonia.csv
  - Columns include Year, Region, Mean occupancy, Lower_CI, Upper_CI, Standard_deviation, Rhat.
- Species trends: long-term growth-rate estimates for the largest region (UK or GB); stored in Species_Trends.csv.
  - Columns include Group, Species, N_Years, First_Year, Last_Year, N_Records, Mean_growth_rate, Lower_CI, Upper_CI, Precision.
- Dataset information and provenance: Datasets_information.csv and Species_Names.csv provide input data coverage, scheme details, start/end years, number of records/species/sites/visits, and name origins/changes for species.

## Considerations for Use
- Uncertainty: occupancy estimates include 95% credible intervals; interpretation should account for posterior uncertainty.
- Coverage variability: taxon- and region-specific coverage, start years (1970 vs 1980), and number of contributing years/records vary by species.
- Data quality: outputs rely on presence-only data with biases (detection, effort, spatial/temporal bias) that are addressed via occupancy modelling; some species are excluded due to insufficient data.
- Upstream information: guidance on usage, dataset specifics, and analysis tools provided in accompanying files (Datasets_information.csv, Species_Trends.csv, Species_Names.csv) and related data paper.

## Tools and Access
- Software: sparta R package for occupancy modelling; BRCindicators R package for trends/indicators (both open source).
- Analysis and visualization: associated Shiny app for viewing occupancy and detection estimates over time (species plots, uncertainty, and trends).
- Citations and references: model methodology and data provenance documented in the accompanying data paper and references linked within the dataset.

## Practical Monitoring Implications
- Enables consistent, region-specific monitoring of biodiversity occupancy and trends across a large suite of taxa.
- Supports multispecies indicators and long-term biodiversity monitoring for action on conservation and policy targets.
- Provides transparent data lineage, quality checks, and documentation to facilitate reuse and integration with other environmental datasets.