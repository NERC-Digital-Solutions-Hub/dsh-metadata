# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- Provides national-scale, annual estimates of species occupancy and trends for 5,293 UK bryophyte, lichen and invertebrate species from 1970 to 2015.
- Outputs include: (i) 1000 posterior occupancy samples per species-region-year, (ii) model-based summary tables (mean occupancy, 95% credible intervals, standard deviation, rhat), and (iii) derived species trend estimates (annual growth rates).
- Outputs are available at multiple regional scales (UK, GB, England, Scotland, Wales, Northern Ireland) depending on input data coverage.
- Data were produced using a Bayesian occupancy modelling framework applied to presence-only occurrence data from volunteer recording schemes, enabling correction for detection and sampling biases.

## Data scope and sources
- Taxonomic scope: 31 taxonomic groups (including 5,293 species with outputs shared).
- Input data: occurrences from 29 schemes plus supplementary records (Biological Records Centre and iRecord), totaling 22,684,449 records for 10,750 species across groups.
- Coverage: occupancy estimates provided for UK, GB, England, Scotland, Wales, and Northern Ireland where data allow; rove beetles (and some others) start in 1980; most groups start in 1970.
- Output subset: only species with at least 50 observations contributed to model output are included.

## Methods and data processing
- Input data standardization:
  - Records must have exact date, 1x1 km grid location, be from 1970 onwards, and occur within the UK.
  - Species names cross-checked with scheme organizers; duplicates removed.
- Modelling approach:
  - Bayesian occupancy models with state (true occupancy) and observation (detection) components to account for imperfect detection and sampling biases.
  - Random walk occupancy framework with country-year effects; list-length categories used in detection.
  - Implemented via occDetFunc in the sparta R package (which uses JAGS for MCMC).
  - Model runs: 40,000 iterations (burn-in 20,000, thinning 3) for small datasets; 20,000 iterations (burn-in 10,000, thinning 3) for larger datasets.
- Outputs:
  - Posterior occupancy: proportion of occupied sites per species-region-year (1000 samples per combination).
  - Convergence: rhat values reported; values ≤ 1.1 indicate convergence.
  - Growth rates: annual percentage growth rates of occupancy, calculated from start to end years for each species using 1000 posterior samples.

## Data formats and files
- Posterior occupancy samples
  - Location: POSTERIOR_SAMPLES folder; one CSV per species.
  - Structure: 1000 rows per region per species, with columns for year (1970–2015, or 1980–2015 for rove beetles), region, iteration, and metadata (Group, Species, Region, Iteration).
- Summary tables
  - Location: SUMMARY_TABLES folder; one CSV per species.
  - Structure: rows by year and region; columns for Mean occupancy, 95% CI (Lower_CI, Upper_CI), Standard_deviation, and Rhat.
- Species trends
  - File: Species_Trends.csv
  - Structure: one row per species with Group, Species, N_Years, First_Year, Last_Year, N_Records, Mean_growth_rate, Lower_CI, Upper_CI, Precision.
- Dataset information and species metadata
  - Datasets_information.csv: country coverage, first/last year, scheme name, N_Records, N_Species, N_Species_Outputs, N_Sites, N_Visits, list-length counts (LL_1, LL_2-3, LL_4+).
  - Species_Names.csv: origin of species names, inclusion status, reasons for any exclusions or name changes.
- Related references and tools
  - R packages: sparta (model fitting) and BRCindicators (trends/indicators).
  - Shiny app: species plots and uncertainty/trend visuals (link provided in the document).

## Considerations for use
- Uncertainty: occupancy estimates come with 95% credible intervals; users should consider uncertainty when applying outputs to decisions.
- Data coverage and comparability:
  - Not all taxa have UK-wide or GB-wide coverage; coverage varies by region and taxon (see Datasets_information.csv).
  - Start years differ (most data begin 1970; rove beetles 1980).
  - Some species have outputs for only a subset of years due to data availability.
- Data quality and interpretation:
  - The dataset emphasizes caution in extrapolation beyond data-supported years for each species.
  - Only species with at least 50 contributing records are included in outputs to ensure informative estimates.
- Outputs useful for:
  - Generating multispecies indicators or trends over time.
  - Informing conservation priorities and monitoring progress toward biodiversity targets.
  - Enabling self-serve exploration through the accompanying Shiny app and programmatic analysis via R packages.

## Access and usage tools
- Shiny app: species-specific plots of occupancy and detection with uncertainty and trend contexts.
- Reproducible workflows: sparta for occupancy modelling; BRCindicators for trends/indicators analysis.
- Documentation and metadata accompanying outputs (Datasets_information.csv, Species_Names.csv) to aid correct interpretation and integration with other datasets.

## Acknowledgements and provenance
- Data contributed by volunteers and recording schemes; supported by Natural Environment Research Council (NERC) funding.