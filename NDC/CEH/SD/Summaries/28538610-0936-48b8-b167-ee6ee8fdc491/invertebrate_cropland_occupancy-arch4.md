# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

## Overview
- A dataset of occupancy estimates for six invertebrate taxa (bees, hoverflies, ladybirds, spiders, carabids, and plant bugs) across three cropland-cover categories (high, low, no cropland) in Great Britain from 1990 to 2019 (with some taxa ending earlier due to data availability).
- Occupancy is the proportion of 1 km grid cells occupied by a species, estimated via hierarchical Bayesian occupancy-detection models.
- Each species-year-region combination includes 999 posterior samples, enabling uncertainty quantification for occupancy trends.
- Data originate from national citizen-science recording schemes, compiled and cleaned to support robust trend analyses.

## Data sources and processing
- Data come from volunteer recording schemes: Bees, Wasps, and Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme.
- Records are presence-only, expert-validated, with efforts standardized to 1 km spatial and day-level temporal precision; records outside 1990–2019 were excluded.
- Taxonomic standardisation performed; mixed taxonomic levels collapsed to species where possible; Harlequin ladybird (an invasive species) removed.
- Detection histories constructed per 1 km site-date using the target-group approach to infer non-detections for focal species; a list-length proxy used as sampling effort.
- Species filtered by data sufficiency thresholds to ensure reliable occupancy estimates.
- Data organized for analysis with the R package sparta.

## Cropland regions and data classification
- Cropland cover per 1 km cell classified into high (>50%), low (0–50%), and no cropland (0%) using Land Cover Map data from 1990 and 2015.
- Cells with cropland-change >10% or with >25% cover of wetlands, built-up, or other classes excluded to improve comparability.
- Regions defined to enable region-specific occupancy trend assessment across cropland intensity.

## Occupancy models
- Species-specific hierarchical Bayesian occupancy-detection models with two submodels:
  - State (occupancy) submodel: occupancy probability varies by year and cropland region, with a site random effect.
  - Observation (detection) submodel: detectability depends on year and list-length category (1; 2–3; ≥4), capturing variation in recording intensity.
- Random-walk prior on year effects allows occupancy trends to evolve smoothly year-to-year.
- Priors are largely uninformative; models fitted using MCMC via the sparta package (3 chains, 32,000 iterations, burn-in 30,000, thinning 6).

## Model outputs and data products
- Occupancy estimates produced as the proportion of occupied sites for each species-year-region.
- Bayesian posterior distributions summarized by 999 sampled occupancies per species-year-region.
- Data format: occ_out_pass.csv containing 4,304,691 occupancy estimates across 34 columns (one column per year; additional columns for iteration, species, taxonomic group, cropland region).
- Not all species-region-year combinations are present; years vary by taxon (bees, hoverflies, ladybirds, and spiders: 1990–2019; carabids and plant bugs: up to 2014 and 2016, respectively).

## Data format details
- Columns include:
  - tax_grp (taxonomic group)
  - species (Latin name)
  - agri (region: high, low, or no_agri)
  - iteration (1–999)
  - year_1990 … year_2019 (occupancy estimates for each year)
- Example rows illustrate a single iteration's year-by-year occupancy values alongside metadata.

## Data quality, limitations, and caveats
- Presence-only data require inference of non-detections via the target-group approach; sampling effort captured only indirectly (list length).
- Occupancy estimates depend on volunteer data quality, spatial/temporal coverage, and the effectiveness of the modelling approach to account for detectability and sampling variation.
- Some taxa have shorter time series; certain years are missing for specific groups due to data availability.
- Exclusion of the Harlequin ladybird and data-sufficiency thresholds aim to improve reliability but may bias representation for certain species.

## Data governance and provenance
- Acknowledges volunteer contributors and funding (NERC grants).
- Methods and model code referenced via related literature and the sparta R package.

## Potential uses for Data Leaders
- Track cross-taxa and cropland-associated occupancy trends to inform data-driven conservation and agricultural policy decisions.
- Compare occupancy dynamics across regions with different cropland intensities to identify data-backed priorities.
- Assess data product usability and identify areas for metadata enhancement, standardization, and potential expansion (e.g., more consistent year ranges or broader taxa).
- Leverage the 999-sample posterior distributions to quantify uncertainty in occupancy projections and support robust decision-making.