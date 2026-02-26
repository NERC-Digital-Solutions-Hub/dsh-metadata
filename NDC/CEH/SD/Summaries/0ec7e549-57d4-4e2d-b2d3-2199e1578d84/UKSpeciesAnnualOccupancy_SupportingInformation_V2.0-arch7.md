# Annual estimates of occupancy for bryophytes, lichens and invertebrates in the UK, 1970-2015

## What this dataset is
- National-scale, annual occupancy estimates and growth-rate trends for 5,293 UK bryophyte, lichen, and invertebrate species from 1970 to 2015.
- Outputs available at multiple regional scales (UK, GB, England, Scotland, Wales, Northern Ireland) where data allow.
- Derived from fine-grained 1x1 km occurrence data using a Bayesian occupancy model; captures occupancy and trends with quantified uncertainty.

## Data scope and coverage
- Taxa: 31 groups including invertebrates, bryophytes, and lichens.
- Regions: UK, GB, England, Scotland, Wales, Northern Ireland (where data permit).
- Years: 1970–2015 (1980–2015 for certain taxa like rove beetles).
- Volume: Input data from 29 recording schemes; 10,750 species and 22,684,449 records processed to produce outputs for 5,293 species.
- Output formats: three forms (posterior samples, summary tables, and species trends).

## Data sources and standardisation
- Input data: presence-only records from UK recording schemes, supplemented with Biological Records Centre (BRC) and iRecord where possible.
- Standardisation criteria: known date to day, location known to 1x1 km, records from 1970 onwards, UK locations; deduplicated and taxonomic names reconciled with scheme guidance.
- Data provenance: details of data sources and counts provided in Datasets_information.csv; 50+ observations threshold used to include species in outputs.

## Modelling approach
- Method: hierarchical Bayesian occupancy modelling (random walk state model with detection process).
- Purpose: account for imperfect detection and various biases in presence-only data, enabling national-scale trend analysis.
- Implementation: occDetFunc in the sparta R package (Bayesian via JAGS); country-year effects in the state model; detection model uses list-length categorisation.
- Iterations and convergence: model runs vary by dataset size (up to 40,000 iterations with burn-in 20,000 for small datasets; 20,000 iterations with burn-in 10,000 for large datasets); convergence assessed with Rhat (target ≤ 1.1).

## Outputs and data formats
- Posterior samples of occupancy
  - Folder: POSTERIOR_SAMPLES; one CSV per species.
  - Each file contains 1000 rows per region (iterations) and columns for year (1970–2015), plus metadata (Group, Species, Region, Iteration).
- Summary tables
  - Folder: SUMMARY_TABLES; one CSV per species.
  - Columns include Year, Region, Mean occupancy, Lower_CI, Upper_CI, Standard_deviation, Rhat.
- Species trends
  - File: Species_Trends.csv
  - Per species: N_Years, First_Year, Last_Year, N_Records, Mean_growth_rate, Lower_CI, Upper_CI, Precision.
  - Growth rates reflect the largest region with data (GB or UK depending on coverage).
- Dataset information
  - File: Datasets_information.csv
  - For each group: country coverage, first/last year, scheme name, N_Records, N_Species, N_Species_Outputs, N_Sites, N_Visits, breakdown by list length (LL_1, LL_2-3, LL_4+).
- Species name information
  - File: Species_Names.csv
  - Origin of names, inclusion status, reasons for exclusion (if any), and details on name changes or aggregations.

## Data accessibility and tools
- R packages
  - sparta: trend estimation for unstructured data (used to run occupancy models).
  - BRCindicators: trends and indicators from biodiversity data.
- Shiny app
  - Interactive viewer for occupancy and detection probabilities, uncertainty, and trend estimates.
  - URL: https://shiny-apps.ceh.ac.uk/speciesplotviewer/
- Associated publications and references
  - Main data paper: Outhwaite et al., 2019 (Scientific Data).
  - Related methodological and governance references provided in the document.

## Guidance for GIS and map-based usage
- Outputs are region-level occupancy proportions with uncertainty, suitable for map-based visualization of biodiversity change over time.
- Use posterior samples to map spatial and temporal uncertainty, not just mean occupancy.
- Check coverage information in datasets (Datasets_information.csv) to understand regional and taxon-specific limits.
- When interpreting trends, consider start/end years and the number of contributing records (N_Years, N_Records in Species_Trends.csv) to assess reliability.
- Data are filtered to species with at least 50 contributing records; some taxa or regions may have gaps.

## Considerations and caveats
- Occupancy estimates are contingent on model assumptions and the quality/coverage of input data; uncertainty is explicitly reported.
- Coverage differs by taxon and region; not all species or regions have UK-wide coverage.
- The largest-region growth-rate summaries are restricted to the region with data for each species.

## Practical notes for use and reproduction
- Outputs are in CSV format and organized by POSTERIOR_SAMPLES, SUMMARY_TABLES, Species_Trends, and supporting information files.
- For analyses replicating or extending this work, the sparta and BRCindicators R packages are available on GitHub, and the occupancy modelling approach can be run using the provided data and code references.
- The accompanying Shiny app provides a quick visual check of species-level occupancy and detection trajectories before deeper GIS analyses.