# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

- What the dataset contains
  - Occupancy estimates for six invertebrate taxa in Great Britain across three cropland cover regions: high, low, and no cropland.
  - Taxa: Apoidea (bees), Syrphidae (hoverflies), Coccinellidae (ladybirds), Arachnida (spiders), Carabidae (carabids), and Heteroptera plant bugs.
  - Time frame: 1990–2019 (with some taxa limited to 1990–2014 or 1990–2016 depending on data availability).
  - Output: 999 posterior samples of occupancy for each species × region × year combination.

- Data sources and cleaning
  - Data come from citizen science recording schemes: Bees, Wasps, and Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme.
  - Records are presence-only and expert-verified; standardized to 1 km spatial precision and day-level temporal precision; time window restricted to 1990–2019.
  - Taxonomic standardization by species; aggregation applied where taxonomy changed over time.
  - Detection histories created per 1 km site × date; non-detections inferred for focal species using other species within the same taxonomic group (target group approach).
  - Sampling effort proxy: list length (number of species recorded per visit).
  - Species filtering: excluded species with insufficient data to yield reliable occupancy trends and Harlequin ladybird (Harmonia axyridis) due to invasion dynamics.
  - Result: species counts by taxon after cleaning (e.g., 224 bees, 221 carabids, 250 hoverflies, 41 ladybirds, 264 plant bugs, 535 spiders).

- Cropland regions and site selection
  - Land Cover data for 1990 and 2015 used to classify 1 km grid cells by cropland cover (arable, perennial crops, etc.).
  - Exclusions to reduce confounding: sites with cropland change >10% removed; sites with >25% presence of wetland, built-up, or other classes removed.
  - Regions defined: high cropland cover (>50%), low cropland cover (0–50%), and no cropland (0%).
  - Occupancy classification per site and year aligned with cropland region.

- Occupancy modeling approach
  - Hierarchical Bayesian occupancy-detection models with two submodels:
    - State (occupancy) model: occupancy probability ψit for site i in year t, varying by cropland region; site random effect ui included.
    - Observation (detection) model: detection probability pitv conditional on occupancy, modeled with year effects and list-length-based data types.
  - Detection probability modeled as a function of data type (list length categories: 1, 2–3, and 4+ species) to account for sampling heterogeneity.
  - Year effects implemented as a random walk prior, enabling smooth temporal changes and information sharing across years.
  - Priors: uninformative priors for most parameters; implemented via MCMC in JAGS through the R package sparta (occDetFunc).
  - Computation: three MCMC chains, 32,000 iterations each, burn-in 30,000, thinning 6.

- Outputs and data format
  - Occupancy estimates: proportion of occupied sites per species per region per year; posterior samples reflect uncertainty.
  - Posterior samples: 999 samples per species × region × year combination; large dataset resulting in 4,304,691 occupancy estimates.
  - Data file: occ_out_pass.csv with 34 columns including year_1990 to year_2019, tax_grp, species, agri (region), iteration, and other metadata.
  - Year coverage and presence:
    - Bees, hoverflies, ladybirds, and spiders span 1990–2019.
    - Carabids and plant bugs have shorter ranges (up to 2014 and 2016, respectively); occupancy estimates missing for years without data.
  - Example structure: one row per iteration; columns for each year (occupancy probability) plus metadata (tax_grp, species, agri, iteration).

- Practical considerations for analysis
  - Data provenance: derived from multiple well-documented citizen science schemes with quality assurance; standardized to enable cross-taxon comparisons by cropland region and year.
  - Handling of imperfect detection: explicit occupancy-detection modeling with a detection process that accounts for sampling effort via list length.
  - Data limitations:
    - Not all species are available in every cropland region; year ranges differ by taxon.
    - Presence-only data require the target-group approach to infer non-detections, which introduces assumptions.
    - Occupancy estimates are averaged over 1 km grid cells; scale may affect detection and occupancy interpretation.
  - Reproducibility and tooling: modelling implemented via sparta’s occDetFunc with JAGS; results are posterior distributions suitable for correlation analyses, trend detection, and cross-taxa comparisons.