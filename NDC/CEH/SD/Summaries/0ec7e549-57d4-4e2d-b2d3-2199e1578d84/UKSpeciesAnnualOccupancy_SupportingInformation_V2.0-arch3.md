# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- Open-access dataset providing national-scale, annual occupancy estimates and trend indicators for 5,293 UK invertebrate, bryophyte and lichen species from 1970 to 2015.
- Outputs cover UK, GB, England, Scotland, Wales, and Northern Ireland where possible; derived from presence-only occurrence records aggregated to 1x1 km squares.
- Uses a Bayesian occupancy modelling framework to account for biases in unstructured occurrence data (e.g., imperfect detection, uneven sampling).
- Outputs include 1,000 posterior samples of occupancy per region-year, summary statistics with credible intervals, and derived annual growth-rate trends.

## What the dataset includes
- Input data: observations from 29 recording schemes plus the Biological Records Centre and iRecord, comprising 22,684,449 records for 10,750 species across 31 taxonomic groups; outputs produced for 5,293 species.
- Regions and years: occupancy estimates at UK, GB, England, Scotland, Wales, and Northern Ireland; years range from 1970 (1980 for some rove beetles) to 2015.
- Data coverage notes: only species with at least 50 observations are included; accompanying metadata includes number of records, sites, and visits.

## Methods
- Data standardization: records must have exact date, 1x1 km location, start 1970 (or 1980 for some taxa), and UK location; species names harmonized with schemes; duplicates removed.
- Occupancy modelling: hierarchical state (occupancy) and observation (detection) components; accounts for detection biases and data collection processes; uses a random-walk occupancy model with country-year effects and list-length as a detection covariate.
- Implementation: models run per species in R using sparta (Bayesian, via JAGS); years span from data start to 2015; iterations differ by dataset size (up to 40,000 total with burn-in and thinning).
- Outputs: posterior distribution of occupancy per region-year; 95% credible intervals; rhat convergence statistic (<= 1.1 considered converged).

## Outputs and data formats
- Posterior samples of occupancy: 1,000 samples per species per region, in separate CSV files (one file per species) with columns for year, region, iteration, and occupancy values.
- Summary tables: one CSV per species detailing mean occupancy, 95% credible intervals, standard deviation, and rhat for each region-year.
- Species trends: a single CSV (Species_Trends.csv) presenting mean annual growth rates for the largest region (UK or GB), with 95% credible intervals, start/end years, number of years, and data coverage.
- Dataset information (Datasets_information.csv): country coverage, start/end years, recording schemes, counts of records/species/sites/visits, and list-length categories.
- Species name information (Species_Names.csv): origin of species names, inclusion status, and notes on name changes or aggregations.

## Considerations for use
- Uncertainty: substantial for many species; use growth-rate and occupancy estimates with their credible intervals to inform decisions.
- Coverage variability: start years, regional coverage, and the number of contributing years differ by species; check accompanying metadata for each taxon.
- Data governance and metadata: extensive metadata provided (datasets, species names, provenance, list-length categories) to support appropriate use and interpretation.

## Tools and access
- R packages: sparta (occupancy/trend estimation) and BRCindicators (change indicators) are provided for analyses.
- Shiny app: interactive viewer for occupancy and detection estimates plus uncertainty and trends (https://shiny-apps.ceh.ac.uk/speciesplotviewer/).
- Citations and data access notes included with the dataset; associated data paper: Outhwaite et al. 2019; Sci. Data 6:259.

## Relevance for monitoring frameworks
- Demonstrates a robust approach to monitoring biodiversity change at national scales using occupancy modelling to handle unstructured data biases.
- Produces interpretable indicators (occupancy, trends, growth rates) with quantified uncertainty suitable for policy scrutiny, performance tracking, and informing future actions.
- Provides rich metadata and open-access tools to support data governance, transparency, and reproducibility in monitoring frameworks.

## Acknowledgements and provenance
- Acknowledges volunteer contributors and recording schemes; funded by Natural Environment Research Council (NE/L008823/1).