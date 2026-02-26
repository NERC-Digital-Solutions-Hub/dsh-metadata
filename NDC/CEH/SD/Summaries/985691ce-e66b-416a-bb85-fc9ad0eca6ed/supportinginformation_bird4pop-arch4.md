# Supporting information for the bird4pop model

- The bird4pop model is a process-based simulator of central-place foraging, nest provisioning, survival, and dispersal for UK passerine birds, iterating to a steady-state landscape carrying capacity. It covers three guilds (woodland specialists, woodland generalists, farmland passerines) and four representative species, and is designed to be continually updated.

## Data inputs and file structure

- Dataset includes code and parameter files required to run bird4pop:
  - Model code and inputs:
    - InputParameters_v7
      - bird_guild_params.csv
      - bird_habitat_params.csv
    - ModelCode
      - run_bird4pop.R
      - computeForageNesting_v3.R
      - getsteadystatepop_v3.R
      - runpop_bird_v3.R
      - growth.func.R
      - latfordisp.R
      - kerncalc.R
  - Landscape input requirements:
    - landscape raster (base landcover), cellsize, edgestack (edge feature rasters), edgecodes (matching landcover codes)
    - fol_c (directory containing R scripts)
    - fol_ip (directory containing input parameter files)
- Input parameter files and columns:
  - bird_guild_params.csv
    - guild_names, guild, growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m, maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv
  - bird_habitat_params.csv
    - guild, Code_ExpOp, nesting, nesting_se, nesting_alpha, nesting_beta, foraging_P1, foraging_P1_se, foraging_P1_alpha, foraging_P1_beta
- Landcover codes and edge handling:
  - Table of landcover codes (0–77) with nesting and foraging resource scores per guild, including edge features (edgestack) used to adjust per-pixel resource values via area-weighted sums.

## Model description and processes

- Short summary:
  - Simulates nesting resource availability, foraging resource availability, foraging effort, nest productivity (via a log-normal relationship with foraging resources), survival (adults and juveniles), and dispersal to new breeding sites, iterating year-by-year until a steady-state population and nesting distribution emerge.
- Core computational steps:
  - Resource mapping:
    - Nesting resources map: nesting score × maximum nest density
    - Foraging resources map: foraging score (0–5) by guild
    - Pixel values are area-weighted sums if multiple landcovers share a pixel (including edge features)
  - Initialization:
    - Random nest sites per pixel from a Poisson distribution around expected nests; nests form breeding pairs
  - Foraging:
    - Fourier transforms convolve nest-origin foragers with the foraging resource map using a distance-decay kernel (defined by foraging range)
    - Estimate foraging rate and resources gathered per pixel
  - Productivity:
    - Productivity (offspring per nest) linked to foraging resources via a log-normal CDF with parameters a (median) and b = 2a
  - Survival:
    - Adult and juvenile survival modeled as separate yearly binomial processes
  - Dispersal:
    - Surviving birds disperse by convolving dispersers with nesting-resource map using a distance-decay kernel (weighted by resources)
    - Arriving dispersers are consolidated into breeding pairs; cap by available nesting sites
  - Iteration and outputs:
    - Iterate across years until steady-state population size and nest distribution are reached
  - Inputs and landscape considerations:
    - Landscape must be a square/rectangular raster with square pixels; wrap-around edges during computation; recommended landscape size and buffering to avoid edge effects
- Implementation details:
  - Core functions and their roles (R):
    - run_bird4pop.R: top-level runner
    - computeForageNesting_v3.R: maps nesting and foraging resources across the landscape
    - getsteadystatepop_v3.R: iterates until steady state
    - runpop_bird_v3.R: simulates a single year's processes
    - kerncalc.R: computes exponential kernels for central-place foraging and dispersal
    - latfordisp.R: applies kernels to place foragers/dispersers on the landscape
    - growth.func.R: defines the population growth function via inverse-logit mapping to offspring
  - These components mirror similar pollination models (poll4pop) and link to openly available code bases.

## Parameterisation and data sources

- Nesting and foraging resource parameters:
  - Derived from an expert-elicitation exercise (n=4 experts) on 77 landcover types, rating nesting (0–1) and foraging (0–5) resources per guild
  - Means and uncertainties (beta-distribution parameters) are provided in bird_habitat_params.csv
  - Foraging scores (0–5) are renormalised to 0–5; nesting scores renormalised to 0–1
  - Beta-distribution parameters enable uncertainty quantification; foraging draws must be scaled by 6 to map beta draws back to 0–5
- Species and guild data:
  - Dispersal ranges from Paradis et al. (1998)
  - Survival probabilities and chicks per year from Robinson (2005)
  - Table of species per guild used to derive guild-level parameter values
- Maximum nest density:
  - Derived from Batten (1976) data; mean nests per hectare per species-community used to derive a guild-agnostic default density: approximately 5 nests ha^-1
- Foraging range and growth calibration:
  - For woodland specialists: foraging range 250 m; growth parameter a = 0.2; growth parameter b = 2a
  - These values applied across guilds/species to maintain proportionality in resource-to-offspring conversion

## Validation and performance

- Validation dataset:
  - Great Britain-wide comparison using the Breeding Bird Survey (BBS) data from 2016–2020 (n = 4,874 survey squares)
  - Abundance index Ai (observed) vs predicted breeding pairs Bi (model)
  - GLM with Poisson error shows a significant positive relationship between predicted and observed abundances for all guilds/species
- Reported relationships (example coefficients):
  - Woodland specialist: β1 ≈ 93.2 (P < 0.001), R^2 ≈ 0.365
  - Woodland generalist: β1 ≈ 36.5 (P < 0.001), R^2 ≈ 0.165
  - Farmland passerine: β1 ≈ 15.8 (P < 0.001), R^2 ≈ 0.010
- Validation references:
  - Gardner et al. (2024) Landscape Ecology
  - Gardner et al. (2020) Methods in Ecology and Evolution
  - Supporting literature for dispersal, survival, landcover parameters, and related calibration

## Outputs

- For each simulated guild, the model produces raster outputs with the same extent/resolution as the input landscape:
  - Nesting resources
  - Breeding season foraging resources
  - Number of adult pairs in the current breeding season
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Juveniles surviving after yearly mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing but before nest-site limitation
  - Adult pairs available for next breeding season after nest-site limitation
  - Foraging rate per pixel during the breeding season
  - Foraging resources gathered per pixel by nesting birds
  - Nest site locations

## Role in decision-making

- The bird4pop model is intended to support decision-makers alongside other ecological information (surveys, local knowledge)
- Outputs should not be used in isolation for policy or management decisions

## Uncertainty, reproducibility, and references

- Uncertainty handling:
  - Habitat resource scores are represented as beta-distributed parameters to enable uncertainty quantification
  - Foraging beta draws require scaling by factor to map back to 0–5 scale
- Reproducibility:
  - Model components are designed to be updated; latest versions and guidance should be sought from the corresponding authors (emmgar@ceh.ac.uk)
  - The computeForageNesting_v3.R function is a minimally-adapted version of computeFloralNesting.R from poll4pop, with public code available at the poll4pop repository (GitHub and Zenodo references)
- References cited within the model documentation:
  - Gardner et al. 2024; Gardner et al. 2020; Hinsley et al. 1996; Paradis et al. 1998; Robinson 2005; Batten 1976; Newson et al. 2009; Siriwardena et al. 1998

## Acknowledgements

- Thanks to volunteer Breeding Bird Survey participants and contributing researchers from CEH and BTO/BirdLife for data and inputs supporting model development and validation