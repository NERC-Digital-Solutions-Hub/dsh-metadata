# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

## Brief description
- Provides occupancy estimates for six invertebrate taxa (Apoidea, Syrphidae, Coccinellidae, Arachnida, Carabidae, Heteroptera plant bugs) across regions of high, low, and no cropland cover in Great Britain from 1990 to 2019.
- Occupancy is the proportion of 1 km grid cells occupied by each species, estimated with a Bayesian occupancy-detection model.
- Outputs include 999 posterior samples per species:year:region combination, enabling uncertainty assessment for monitoring and decision-making.
- Data derived from observations collected by national recording schemes and societies and compiled for model input.

## Data sources and sampling design
- Data from multiple citizen-science schemes: Bees, Wasps, and Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme.
- Records are presence-only and field-verified by taxon experts; records span decades with large national coverage.
- Records cleaned and standardized: spatial (1 km) and temporal (day) precision, limited to 1990–2019, taxonomic levels restricted to species or aggregated species where appropriate.
- Detection histories built per site/date; non-detections inferred for focal groups using a “target group” approach; sampling effort proxied by list length (number of species recorded per visit).
- Species with insufficient data or with biases (e.g., Harlequin ladybird) excluded to improve reliability.

## Cropland regions and data preparation
- Cropland cover categories derived from Land Cover maps for 1990 and 2015 (25 m resolution; 15 classes). Cropland includes arable and perennial crops and freshly ploughed land.
- Sites with cropland cover change >10% between 1990 and 2015 were discarded; sites with >25% cover of wetlands, built-up, or other classes were excluded for comparability.
- Regions classified as high cropland (>50%), low cropland (0–50%), and no cropland (0%) using an empirical distribution of cropland cover, based on Land Cover Map 2015.

## Occupancy models and statistical approach
- For each species, hierarchical Bayesian occupancy-detection models are fitted to detection histories.
- State sub-model: occupancy z_it ~ Bernoulli(ψ_it); logit(ψ_it) varies by year and cropland region with site random effects.
- Observation sub-model: detection probability p_itv depends on year effects and list-length categories (1; 2–3; 4+), capturing variation in recording intensity.
- Year effects for occupancy modeled with a random walk prior to smooth year-to-year changes; weakly informative priors for other parameters.
- Models fitted with occDetFunc (R, sparta package) using MCMC: 3 chains, 32,000 iterations, burn-in 30,000, thinning 6.

## Outputs and data format
- Occupancy estimates represent the proportion of occupied sites per region (high, low, no cropland).
- Posterior distributions produced for each year and region; 999 posterior samples extracted for each species:year:region combination.
- Data file: occ_out_pass.csv containing 4,304,691 occupancy estimates across 34 columns (one per year; plus metadata: tax_grp, species, agri, iteration).
- Taxa and years included vary by group:
  - Bees, hoverflies, ladybirds, and spiders: 1990–2019.
  - Carabids: up to 2014.
  - Plant bugs: up to 2016.
- Not all species appear in all cropland regions; some region/year combinations are absent due to data availability.

## Data governance, sharing, and accessibility
- Outputs provide explicit uncertainty through posterior samples to support monitoring decisions and scenario analysis.
- Data are derived from publicly contributed citizen science data, with transparent processing and modelling steps described.
- Data cleaning, standardization, and model specifications are documented to support reproducibility and auditability.

## Limitations and considerations for monitoring
- Presence-only data require inference of non-detections via the target-group approach, which introduces assumptions.
- Data availability and recording effort vary by taxon and year, leading to uneven temporal coverage across groups.
- Exclusion of certain species and changes in taxonomy during the study period affect comparability.
- Cropland classification relies on 1990/2015 land-cover maps; changes in land use outside these snapshots are not captured.