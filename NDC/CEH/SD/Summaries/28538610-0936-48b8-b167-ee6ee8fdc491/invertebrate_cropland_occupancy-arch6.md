# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

- Overview
  - A dataset of occupancy estimates for six invertebrate taxa (Bees, Hoverflies, Ladybirds, Spiders, Carabids, Plant bugs) across three cropland-cover regions (high, low, no cropland) in Great Britain from 1990 to 2019.
  - Occupancy is the proportion of 1 km grid cells occupied by each species, estimated via a Bayesian occupancy-detection model.
  - For each species:year:region, 999 posterior samples of occupancy are provided.

- Data sources and processing
  - Data come from volunteer recording schemes: Bees/Wasps/Ants Recording Society, Hoverfly Recording Scheme, UK Ladybird Survey, Ground Beetle Recording Scheme, Terrestrial Heteroptera Recording Scheme, Spider Recording Scheme.
  - Records are presence-only with expert verification; spatial (1 km) and temporal (day) precision standardised; records outside 1990–2019 excluded.
  - Taxonomy cleaned to species level (with some aggregates); data organized into detection histories using formatOccData from the sparta R package.
  - Non-detections inferred via the target-group approach; sampling effort proxied by list length.
  - Species filtered to exclude imprecise cases and the Harlequin ladybird (Harmonia axyridis).
  - Resulting taxon-year species counts: 224 bees, 221 carabids, 250 hoverflies, 41 ladybirds, 264 plant bugs, 535 spiders.

- Cropland regions
  - Cropland coverage classified per 1 km cell using Land Cover Maps for 1990 and 2015 (25 m resolution, 15 classes).
  - Exclusions: sites with cropland change >10%; sites with >25% wetland, built-up areas, or other classes excluded.
  - Regions defined by cropland share: high (>50%), low (0–50%), no cropland (0%).
  - Land cover data used to align occupancy trends with cropland contexts.

- Occupancy models
  - Hierarchical Bayesian occupancy-detection models with:
    - State sub-model: occupancy probability ψ_it for site i in year t, varying by cropland region; includes site random effect u_i.
    - Observation sub-model: detection probability p_itv for visit v, conditional on true occupancy; models time trend a_t and list-length categories (data types 1, 2–3, 4+).
  - Year effects are region-specific; random-walk prior on year effects to ensure smooth temporal changes.
  - Model fitting via occDetFunc (sparta package) using MCMC in JAGS: 3 chains, 32,000 iterations, burn-in 30,000, thinning factor 6.

- Model outputs
  - Occupancy estimates reported as posterior distributions for each region, year, and species.
  - 999 posterior samples retained per species:year:region combination.

- Data format and availability
  - Data file: occ_out_pass.csv containing 4,304,691 occupancy estimates across 34 columns (one per year plus identifiers).
  - Columns include: tax_grp (taxonomic group), species (Latin name), agri (region: high, low, no_agri), iteration (1–999), year_1990 to year_2019.
  - Not all species appear in all cropland regions; year ranges vary by taxon (Bees, Hoverflies, Ladybirds, Spiders: 1990–2019; Carabids: up to 2014; Plant Bugs: up to 2016).

- Acknowledgements
  - Thanks to volunteers and contributing schemes; funding by NERC grants NE/S000100/1 and NE/V007548/1.