# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

## Overview
- Dataset provides occupancy estimates for six invertebrate taxa in Great Britain across three cropland-cover regimes (high, low, no cropland) from 1990 to 2019 (with some taxa extending to 2014–2016).
- Occupancy = proportion of 1 km grid cells occupied by a species, estimated via Bayesian occupancy-detection models.
- Outputs include 999 posterior samples per species × year × region, enabling assessment of trends and uncertainty.

## Data sources and processing
- Data originate from citizen science recording schemes: Bees, Wasps, and Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme.
- Records are presence-only, vetting by taxon experts; cleaned to ensure spatial (1 km) and temporal (day) precision; years limited to 1990–2019 (with earlier/later limits due to data constraints).
- Taxonomy standardized to species level; Harlequin ladybird removed due to invasion-driven trends.
- Detection histories created per 1 km site × date; non-detections inferred via a target-group approach using other species in the same taxonomic group; sampling effort proxied by list length (number of species recorded on a visit).

## Cropland regions
- Cropland cover classified per 1 km cell using Land Cover maps for 1990 and 2015 (25 m resolution; 15 classes).
- Excluded sites with cropland-change >10% and sites with >25% coverage of wetlands, built-up, or other classes.
- Regions defined by empirical cumulative distribution: high cropland (>50%), low cropland (0–50%), no cropland (0%).

## Occupancy models
- Species-specific hierarchical Bayesian occupancy-detection models with two submodels:
  - State sub-model: true occupancy z_it ~ Bernoulli(ψ_it); year effects differ by cropland region; site random effects included.
  - Observation sub-model: detection probability p_itv for visit v, conditional on occupancy; modeled as function of year effect and list-length category (datatype) with categories: list length 1; 2–3; 4+.
- Detectability parameters β1, β2 quantify differences by list length relative to a 1-species list.
- Year effects follow a random walk prior to enable smooth temporal changes; uninformative priors for other parameters.
- fitting method: occDetFunc (R package sparta) using MCMC via JAGS; 3 chains × 32,000 iterations; burn-in 30,000; thinning 6.

## Model outputs
- Occupancy: proportion of occupied sites per species × region (high/low/no cropland).
- Posterior: 999 samples per year × species × region.
- Outputs stored as a large posterior-sample dataset; future analyses can compare trends across cropland regimes with quantified uncertainty.

## Data format and availability
- Primary data file: occ_out_pass.csv
  - Contains 4,304,691 occupancy estimates across 34 columns.
  - Columns include: tax_grp, species, agri (region: high/low/no_agri), iteration (1–999), year_1990 to year_2019.
- Not all species appear in all cropland regions; year ranges differ by taxon:
  - Bees, Hoverflies, Ladybirds, Spiders: 1990–2019.
  - Carabids: up to 2014.
  - Plant bugs: up to 2016.
- Table-like example: rows show per-iteration occupancy values for consecutive years, with metadata columns (tax_grp, species, agri, iteration).

## Acknowledgements and references
- Acknowledgment of volunteers and recording schemes; funding from NERC grants.
- References include methodological and data-source papers on occupancy modelling, citizen science data, and data-processing approaches used in the study.

## Relevance for environmental monitoring
- Provides a standardized, long-term, region-stratified occupancy framework for six invertebrate groups across gradients of cropland.
- Accounts for imperfect detection and variable sampling effort, enabling robust monitoring of environmental health and policy performance over time.
- Data and methods support integration with other datasets to enhance the value and accessibility of monitoring outputs.