# Data Overview

- What the data are
  - Outputs from ensemble Species Distribution Models (SDMs) used to explore how socio-political factors affect bird and mammal biodiversity under climate change.
  - Three CSV datasets are provided:
    - Climate_impacts_by_country.csv (national-level impacts for 189 countries)
    - transboundary_richness.csv (current intersections of species ranges with political borders)
    - transboundary_range_shifts.csv (projected cross-border range shifts under climate change)

- Data scope and coverage
  - Global spatial scope covering more than 12,700 terrestrial birds and mammals (about 80% of species with broad ranges; restricted-range species excluded).
  - National analysis focuses on changes in species richness projected to 2070 and relates them to governance indicators.
  - Transboundary analyses assess how species ranges intersect borders now and how many are projected to cross borders under climate change.

- Data generation methods
  - SDMs: ensemble of four model types — Generalised Additive Models (GAMs), Generalised Linear Models (GLMs), Random Forests (RFs), and Boosted Regression Trees (BRTs).
  - Predictors: mean annual temperature, temperature seasonality, precipitation in wettest and driest months, and precipitation seasonality.
  - Climate projections: four scenarios (RCP 2.6, 4.5, 6.0, 8.5) for 2070, using three GCMs (HadGEM2-ES, CCSM4, MIROC-ESM-CHEM).
  - Spatial validation: data split into ten spatial blocks; 10-fold cross-validation; performance assessed with AUC.
  - Projections: for each species, an ensemble of 120 projections (4 models × 10 blocks × 3 GCMs) per climate scenario; mean presence/absence weighted by model AUC to yield final species distributions.
  - Aggregation: grid-cell richness aggregated to national level (mean across grid cells per country) for current and 2070 under each scenario.

- Data structure and units
  - Climate_impacts_by_country.csv
    - 189 rows (one per country); 31 columns.
    - First column: ISO3 country code.
    - Last column: governance score (mean of six World Bank Governance Indicators; range -2.5 to 2.5) using 2018 data.
    - Middle columns: scenario × taxon × measurement (e.g., rcp85_bird_SR; current_mammal_pctChange).
  - Transboundary_richness.csv
    - 327 rows (one per border); 3 columns.
    - Border identifier; transboundary_richness (number of species whose ranges intersect the border); transboundary_richness_threatened (number of threatened species intersecting the border).
  - Transboundary_range_shifts.csv
    - 6 columns.
    - Border identifier; projected transboundary range shifts by border broken down by taxon (mammals, birds) and scenario (RCP4.5, RCP8.5); barrier_species (non-flying mammals crossing fortified borders under high emissions) with NA where no barrier exists.

- Data sources and provenance
  - Species data from IUCN Red List of Threatened Species and BirdLife International / Handbook of the Birds of the World.
  - Climate projections aligned with IPCC scenarios and GCMs as noted above.
  - Governance indicators sourced from World Bank Governance Indicators (2018).
  - Spatial border data via rworldmap; analyses using raster packages in R.
  - Contextual methodology described in Titley et al., 2021 (PNAS).

- Reproducibility and notes
  - Extensive cross-validation and model weighting based on AUC enhance robustness.
  - National governance scores provide a standardized contextual variable for comparing climate-biodiversity impacts across countries.
  - Data intended to support cross-border conservation planning, assessment of governance relationships, and exploration of global inequities in conservation under climate change.