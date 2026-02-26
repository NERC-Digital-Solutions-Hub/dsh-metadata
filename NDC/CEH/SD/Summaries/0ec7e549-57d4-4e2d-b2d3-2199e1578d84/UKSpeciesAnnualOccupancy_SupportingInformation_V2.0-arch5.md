# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK (1970 - 2015)

## Overview
- Provides national-scale, annual occupancy estimates and growth-rate trends for 5,293 UK invertebrate, bryophyte, and lichen species from 1970 to 2015.
- Outputs include country/region-level estimates (UK, GB, England, Scotland, Wales, Northern Ireland) where data permit.
- Derived from fine-grained input data (1x1 km squares) using a Bayesian occupancy model applied to presence-only records.
- Large input dataset compiled from 29 national recording schemes and societies, totaling 22,684,449 records; model outputs shared for species with at least 50 observations.
- Associated with an open-access data paper (Outhwaite et al., 2019) and supplementary materials, plus an online Shiny viewer.

## Data provenance and governance
- Input data drawn from UK recording schemes, supplemented by Biological Records Centre (BRC) and iRecord where possible.
- Standardisation criteria applied to inputs (date known to day; location to 1x1 km; records from 1970+; UK location).
- Metadata and provenance documented in accompanying files:
  - Datasets_information.csv (country coverage, year ranges, data sources, counts of records/species/sites/visits, list-length categories).
  - Species_Names.csv (name origins, inclusion status, details on changes/aggregations).
- Data are open access and intended for multispecies indicators and national biodiversity monitoring.

## Methods and data quality
- Modelling approach: occupancy models with a state component (true occupancy) and an observation component (detection process) to address biases in presence-only data.
- Framework: random-walk occupancy model with country-year effects; detection modeled with list length categorisation.
- Implementation: occDetFunc in the sparta R package (Bayesian inference via JAGS); runs 1970–2015 (1980–2015 for rove beetles).
- Uncertainty and convergence: posterior distributions produced; 1000 samples per species-region-year provided; convergence assessed with Rhat (≤1.1 considered converged).
- Data scope notes: outputs include only species with adequate data; some taxa have shorter time spans or regional coverage than others.

## Outputs and data formats
- Three main output forms (CSV, organized in folders):
  - Posterior samples: 1000 occupancy samples per species per region across years (POSTERIOR_SAMPLES). Each file includes 1000 x number-of-regions rows and columns for year occupancy estimates plus metadata (Group, Species, Region, Iteration).
  - Summary tables: occupancy statistics per year and region (SUMMARY_TABLES). Columns include mean occupancy, 95% credible intervals, standard deviation, and Rhat.
  - Species trends: long-term annual growth-rate estimates for the largest region (UK or GB) (Species_Trends.csv). Includes N_Years, First_Year, Last_Year, N_Records, Mean_growth_rate, Lower_CI, Upper_CI, and Precision.
- Additional context files: Datasets_information.csv (data coverage and input details by taxon) and Species_Names.csv (name origins and inclusion notes).
- Data formats are CSVs; naming conventions described (e.g., AnnualSpeciesOccupancy_PosteriorSamples_[Group]_[Species].csv).

## Usage considerations for data stewards
- Uncertainty: occupancy estimates carry substantial uncertainty; users should consider 95% credible intervals and the number of contributing records for each species.
- Coverage variability: start years, regional coverage, and number of contributing years vary by species; refer to Datasets_information.csv and Species_Trends.csv for specifics.
- Non-extrapolation: trends are calculated only over years with available data for each species to avoid extrapolation beyond the input data.
- Metadata richness: extensive provenance, data source details, and name-origin information support robust data governance and reproducibility.

## Tools and access
- R packages:
  - sparta: for occupancy trend analysis of unstructured data (used to run models) – https://github.com/BiologicalRecordsCentre/sparta
  - BRCindicators: for trends/indicators from occupancy data – https://github.com/BiologicalRecordsCentre/BRCindicators
- Shiny app: species-level plots of occupancy and detection with uncertainty and trend estimates (https://shiny-apps.ceh.ac.uk/speciesplotviewer/)
- Citations provided in the data paper; dataset is part of Scientific Data open-access publication (Outhwaite et al., 2019).

## Practical context and purpose
- Aims to inform biodiversity monitoring and conservation action by providing high-level, fine-grained occupancy information across multiple UK taxa.
- Enables national indicators and comparisons over time, while acknowledging biases and data gaps inherent in citizen-science–type input data.
- Supports data governance through documented data sources, standardisation rules, and accessibility of raw posterior samples alongside derived summaries.