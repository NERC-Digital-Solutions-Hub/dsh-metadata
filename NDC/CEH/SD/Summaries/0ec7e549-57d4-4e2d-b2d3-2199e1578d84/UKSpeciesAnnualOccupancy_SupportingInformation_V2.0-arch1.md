# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- Provides national-scale, annual occupancy estimates and trends for 5,293 UK species across bryophytes, lichens, and invertebrates from 1970 to 2015.
- Outputs are derived from 1x1 km square data and derived at multiple regional scales (UK, GB, England, Scotland, Wales, Northern Ireland) where possible.
- Data generated from presence-only occurrence records aggregated from 29 recording schemes, totaling 22,684,449 records, using a Bayesian occupancy model.
- Outputs include: 1000 posterior samples of occupancy per species-region-year, summary tables with occupancy statistics, and derived annual growth-rate trends.
- The dataset and methods are described in Outhwaite et al. (2019) Scientific Data; data are open access. An accompanying Shiny app provides interactive visualization.

## Data scope and input data
- Input scope: 10,750 species from 31 taxonomic groups; focused on bryophytes, lichens, and invertebrates; 5,293 species have outputs shared here.
- Data sources: 29 recording schemes; supplemented with Biological Records Centre (BRC) data and iRecord where helpful.
- Data quality criteria for inputs:
  - Date known to the day
  - Location known to 1x1 km
  - Records from 1970 onwards (1980 start for rove beetles)
  - Location within the UK (England, Northern Ireland, Scotland, Wales)
  - Taxonomic names checked and duplicates removed
- Rationale: Occurrence data are presence-only and biased; occupancy modelling accounts for imperfect detection and sampling biases.

## Modelling approach
- Method: Bayesian occupancy models using a hierarchical framework with a state model (true occupancy) and an observation model (detection process).
- Framework: Random walk occupancy model with country-level year effects; list-length category incorporated into detection.
- Implementation: occDetFunc in the R package sparta; runs via JAGS; 1970 (or 1980 for some taxa) to 2015.
- Outputs per species: posterior samples for occupancy by region and year; 1000 samples retained for practical use.
- Convergence and iteration: small datasets ~40,000 iterations; large datasets ~20,000 iterations with burn-in and thinning; convergence assessed via rhat (≤ 1.1 considered converged).

## Outputs and data structure
- Posterior samples of occupancy
  - 1000 samples per species-region-year, stored as separate CSV files in POSTERIOR_SAMPLES.
  - Each file includes 50 columns: year columns (1970–2015), plus species, group, region, and iteration identifiers.
- Summary tables of occupancy
  - One CSV per species in SUMMARY_TABLES.
  - Columns per row: year, region, mean occupancy, 95% credible interval (Lower_CI, Upper_CI), standard deviation, and Rhat.
- Species trends
  - Species_Trends.csv contains mean annual growth rate (percentage) for the largest region (UK or GB), with 95% credible intervals, and precision.
  - Includes N_Years, First_Year, Last_Year, N_Records, and data coverage notes for each species.
- Dataset information and species metadata
  - Datasets_information.csv: country coverage, first/last year of input data, scheme details, counts of records/species/sites/visits, and list-length category counts (LL_1, LL_2-3, LL_4+).
  - Species_Names.csv: origins of species names, inclusion status in final dataset, and notes on name changes or aggregations.

## Considerations for use
- Uncertainty and data coverage vary by species and region; use occupancy and trend estimates with their 95% credible intervals to assess reliability.
- Start and end years, coverage by region, and number of contributing years differ by species; details are provided in the accompanying datasets information.
- Some taxa have shorter time series or GB vs UK coverage; extrapolation beyond data is not recommended.
- The Shiny app offers interactive plots of occupancy and detection estimates over time but species-level outputs should be interpreted with care when used for single-species decisions outside multispecies indicators.

## Tools and resources
- R packages
  - sparta: occupancy-trend estimation for unstructured data; used to run the models.
  - BRCindicators: trends and indicators from occurrence data.
- Shiny app
  - Interactive viewer for species-level occupancy and detection estimates over time: https://shiny-apps.ceh.ac.uk/speciesplotviewer/
- Citations and data usage
  - Primary data paper: Outhwaite et al., 2019, Scientific Data.
  - Related methodological references provided in the document.
- Acknowledgments and funding
  - Volunteer contributors and recording schemes; funded by Natural Environment Research Council (NERC), award NE/L008823/1.

## Data provenance and naming
- Species names originate from direct scheme datasets or BRC concept code mappings.
- The dataset includes only species with at least 50 contributing records; per-species details provided in Species_Names.csv.
- Full methodology and validation described in the accompanying data paper (Outhwaite et al., 2019).