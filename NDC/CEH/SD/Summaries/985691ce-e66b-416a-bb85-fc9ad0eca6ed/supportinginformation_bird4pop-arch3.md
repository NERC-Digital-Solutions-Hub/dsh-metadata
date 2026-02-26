# Supporting information for the bird4pop model

## Overview
- A process-based model to simulate central-place foraging and population dynamics of UK passerine birds during the breeding season.
- Models nest site use, foraging effort, survival, and dispersal to estimate steady-state landscape carrying capacity.
- Parameterised for three bird guilds (woodland specialists, woodland generalists, farmland passerines) and four example species; suitable for extending to additional species/guilds.
- Outputs a suite of rasters per guild detailing nesting resources, foraging resources, population sizes, survival, dispersal, and nest locations.
- Intended to support, not replace, decision-making; outputs should be interpreted alongside other ecological information.

## Model description and processes
- Short summary: central-place foraging around nests; offspring production depends on forage; dispersal and mortality shape annual population; iterates to reach landscape steady state.
- Key computational steps:
  - Landscape decomposition into nesting resource map and breeding-season foraging resource map, with edge features (e.g., hedgerows) treated as sub-pixel contributions.
  - Random initial nest placement per pixel based on nesting resource density; nests host breeding pairs.
  - Foraging calculation using Fourier transforms to convolve nest locations with the foraging resource map; creates a foraging-rate field and estimates forage gathered per pixel.
  - Population growth linking nest productivity to gathered resources via a log-normal cumulative distribution (parameters a, b).
  - Annual survival with separate adult and juvenile survival probabilities; survivors breed and disperse.
  - Dispersal modeled by convolution with a nesting-resource-weighted distance-decay kernel; dispersers consolidate into breeding pairs with a 50:50 sex ratio and a cap on nests per pixel based on nesting resources.
  - Iteration across years until steady-state population size; final nest distribution reflects resource availability and dispersal reach.
- Required inputs and structure:
  - Landscape raster (base landcover), cellsize, edge feature rasters (edgestack) and corresponding edgecodes.
  - Guild definitions (guilds) and directories containing model scripts and inputs (fol_c and fol_ip).
  - Input parameter files:
    - bird_guild_params.csv: includes guild_names, growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m, maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv, and related fields.
    - bird_habitat_params.csv: includes guild, Code_ExpOp, nesting, nesting_se, nesting_alpha, nesting_beta, foraging_P1, foraging_P1_se, foraging_P1_alpha, foraging_P1_beta, with landcover codes aligned to the landscape.
- Core R functions (with external dependencies):
  - run_bird4pop.R: top-level model driver.
  - computeForageNesting_v3.R: maps nesting and foraging resources across the landscape (adapted from poll4pop workflow).
  - getsteadystatepop_v3.R: iterates yearly runs to reach steady state.
  - runpop_bird_v3.R: simulates a single-year year’s foraging, nest location, survival, and dispersal.
  - kerncalc.R: computes exponential distance kernels for central-place foraging and dispersal.
  - latfordisp.R: applies kernels to distribute foragers and dispersers, weighted by resources.
  - growth.func.R: defines the inverse-logit based population growth function.
- Notes on provenance and interoperability:
  - Several functions are identical copies of components from the poll4pop model (with links to the GitHub repository).
  - The model is designed for reuse and uncertainty analysis via beta-distributed resource scores.

## Data inputs, files, and parameters
- Landscape inputs:
  - landscape raster: square/rectangular extent, pixel-based landcover codes matching bird_habitat_params.csv.
  - cellsize: pixel size in meters.
  - edgestack: stack of edge feature rasters describing area within each pixel covered by sub-pixel features.
  - edgecodes: corresponding landcover codes for each edge feature.
  - guilds: names of bird guilds to simulate, matching bird_guild_params.csv.
  - fol_c and fol_ip: directories containing the model scripts and input parameter files, respectively.
- bird_guild_params.csv (required columns):
  - guild_names, guild, growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m, maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv (plus optional standard error columns in archived versions).
- bird_habitat_params.csv (required columns):
  - guild, Code_ExpOp, nesting, nesting_se, nesting_alpha, nesting_beta, foraging_P1, foraging_P1_se, foraging_P1_alpha, foraging_P1_beta.
- Outputs per guild:
  - Nesting resources
  - Breeding season foraging resources
  - Number of adult pairs in current breeding season
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Offspring surviving after yearly mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing and before nest-site limitation
  - Adult pairs available for next season after nest-site limitation
  - Foraging rate per pixel during breeding season
  - Foraging resources gathered per pixel
  - Nest site locations

## Parameterisation and calibration
- Nesting and foraging resource parameters (expert opinion):
  - Expert elicitation from four CEH/BTO researchers across 77 landcover types to rate nesting (0–1) and foraging (0–5) resources per guild.
  - Means and beta-distribution parameters included for uncertainty quantification; nesting scores renormalised to 0–1; foraging scores kept on 0–5 scale (with appropriate beta parameters scaled for 0–5).
- Dispersal, survival, and chick production (literature-based):
  - Dispersal ranges drawn from Paradis et al. (1998); guild-level values derived from species lists weighted by breeding territory numbers.
  - Survival probabilities and chicks per year derived from Robinson (2005).
- Maximum nest density:
  - Derived from Batten (1976) data for oakwood plots; mean across guilds standardized to approximately 5 nests per hectare (applied uniformly across guilds for model simplicity).
- Foraging range and population growth calibration:
  - Woodland specialists: foraging range ~250 m; growth parameter a ~0.2; b set to 2a; calibration aimed to align predictions with patch occupancy trends and resource-limited vs. resource-limited regimes.
- Validation approach:
  - GB-wide comparison against Breeding Bird Survey (BBS) 2016–2020 data (n=4874 squares).
  - Relationship between predicted breeding-pair abundance and observed relative abundance tested with a Poisson GLM; significant positive relationships across all guilds (with guild-specific coefficients and R-squared values reported).

## Model validation results
- For woodland specialists, woodland generalists, and farmland passerines, model predictions showed significant positive relationships with observed BBS counts.
- Coefficients (β1) and significance levels indicate robust associations, supporting the model’s utility for relative abundance and distribution patterns within the study area.

## Role in decision-making
- Bird4pop and similar 4pop models are intended to inform decisions alongside other ecological data (surveys, local knowledge).
- Do not rely on model outputs in isolation; consider local conditions, behaviour, and data quality; use outputs to explore scenarios, resource dependence, and landscape-level carrying capacity.

## Acknowledgements
- Thanks to Breeding Bird Survey volunteer surveyors and contributing organizations (BTO/RSPB/JNCC).

## References
- Includes key sources for landcover coding, dispersal, survival, growth, and prior related modelling work (Gardner et al. 2020, 2024; Hinsley et al. 1996; Paradis et al. 1998; Robinson 2005; Batten 1976; Eaton & Noble 2021; and related poll4pop documentation).