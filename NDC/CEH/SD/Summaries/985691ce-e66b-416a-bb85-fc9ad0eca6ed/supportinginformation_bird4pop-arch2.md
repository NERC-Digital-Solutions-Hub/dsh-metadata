# Supporting information for the bird4pop model

## 1. Model description

- Bird4pop is a process-based model that simulates central-place optimal foraging of nidicolous birds around nests during the breeding season. Offspring output depends on forage resources and the landscape’s carrying capacity. Adults and offspring disperse across the landscape, with separate survival for adults and juveniles.
- The model iterates over multiple years to reach a steady-state carrying capacity and is parameterised/validated for 3 bird guilds (woodland specialists, woodland generalists, edge-nesting farmland passerines) and 4 species (nuthatch, robin, yellowhammer, skylark).
- Outputs include a suite of rasters per guild that quantify nesting and foraging resources, population dynamics, survival, dispersal, and nest locations.

## 2. Computational processes

- Resource mapping
  - Nesting resources map: nesting attractiveness (0–1) × maximum nest density for the guild.
  - Breeding-season foraging resources map: foraging resource scores (0–5) by landcover for the guild.
  - Edge features (e.g., hedgerows) are integrated as area-weighted sums per pixel when present.
- Initialization
  - Nest sites are randomly allocated per pixel from a Poisson distribution around expected nests; each nest begins with a breeding pair.
- Foraging
  - A Fourier-transform-based convolution links nest locations to the foraging resources map using a distance-decay kernel (based on foraging range).
  - Calculates per-pixel foraging rates and how much resources foragers gather from their surroundings.
- Population growth
  - Nest productivity (offspring per nest) relates to foraging resources via a log-normal CDF with median a and variance b = 2a.
- Survival and reproduction
  - End-of-season survival is determined by binomial draws with separate adult and juvenile survival probabilities.
  - Offspring that survive reach breeding age and join the breeding population.
- Dispersal and pairing
  - Survivors disperse by convolving dispersers with nesting resources, using a distance-decay kernel weighted by dispersal distance.
  - Arriving dispersers form breeding pairs (50:50 sex ratio); breeding pairs per pixel cannot exceed the nesting-resource–driven capacity.
- Iteration to steady-state
  - The process repeats with the surviving cohort forming the next breeding population until landscape carrying capacity stabilizes.
  - Final nest distribution favors areas with adequate foraging resources or proximity to more productive areas; offspring production reflects local resource availability.
- Inputs
  - landscape raster (base landcover), cellsize, edgestack (edge habitats), edgecodes (matching landcover codes), guilds, fol_c (model scripts), fol_ip (input parameters).
  - Input parameter files: bird_guild_params.csv and bird_habitat_params.csv (guild- and landcover-specific parameters).

## 3. Model outputs

- For each simulated guild:
  - Nesting resources
  - Breeding-season foraging resources
  - Number of adult pairs in the current breeding season
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Offspring surviving after yearly mortality
  - Total surviving birds after dispersal to new breeding sites
  - Adult pairs after pairing up surviving birds but before nest-site limitation
  - Adult pairs available for next breeding season after nest-site limitation
  - Foraging rate per pixel during the breeding season
  - Foraging resources gathered per pixel during the breeding season
  - Nest site locations

## 4. Model parameterisation

- Guilds and species
  - Parameterised for three guilds and four representative species (nuthatch, robin, yellowhammer, skylark).
- 2.1 Nesting and foraging resource parameters: expert opinion data
  - Four experts provided landcover-specific nesting and foraging scores (0–1 for nesting; 0–5 for foraging) across 77 landcover types.
  - Means and uncertainty (beta distributions) are stored in bird_habitat_params.csv; nesting scores renormalised to 0–1 and foraging scores remain on 0–5.
  - Beta-distribution parameters enable uncertainty analyses; foraging draws must be multiplied by six when converting from the 0–1 scale to the 0–5 scale for random draws.
- 2.2 Dispersal, survival and chick production parameters: literature data
  - Dispersal ranges derived as abundance-weighted means (Paradis 1998; Robinson 2005), combined across species within each guild.
  - Survival probabilities and mean chicks per year derived from Robinson (2005) (broods × clutch size).
  - Table mappings link guilds to constituent species.
- 2.3 Maximum nest density parameter: derivation
  - Based on Batten (1976) across oakwood plots; converted to territories per hectare and averaged across plots.
  - Guilds modelled (woodland specialist, woodland generalist, farmland) assumed Nspecies values of 9, 10, and 5, respectively; mean maximum nest density D ≈ 5 nests ha−1 used for simplicity across all guilds.
- 2.4 Foraging range and population growth parameters: calibration
  - Foraging range set to 250 m; growth parameter a = 0.2; growth parameter b = 2a.
  - Values chosen to align predictions with patch-size–dependent occupancy and resource-limited vs. forage-limited dynamics.

## 5. Model validation

- Validation against Breeding Bird Survey (BBS) data for 2016–2020 across Great Britain (n = 4,874 squares).
- Relationship tested: observed relative abundance (Ai) vs. model-predicted breeding pairs (Bi) per square, using a Poisson GLM: ln(Ai) = β0 + β1Bi.
- Results show significant positive relationships for all three guilds/species parameterisations, indicating concordance between model outputs and observed bird abundance (specific β1, standard error, P-values, and R2 values reported for each case).

## 6. Role in decision-making

- The bird4pop family of models is intended to support environmental decisions alongside other ecological information (field surveys, local knowledge).
- Outputs should not be used in isolation; site-specific conditions and species behavior can differ from model inputs and assumptions.

## 7. Reproducibility, data, and code

- The dataset includes model code and parameter files required to run bird4pop (InputParameters_v7, bird_guild_params.csv, bird_habitat_params.csv, and several R scripts).
- Core R functions:
  - run_bird4pop.R (top-level)
  - computeForageNesting_v3.R
  - getsteadystatepop_v3.R
  - runpop_bird_v3.R
  - kerncalc.R
  - latfordisp.R
  - growth.func.R
- The computeForageNesting_v3.R function is a minimally adapted version of computeFloralNesting.R from poll4pop (GitHub: yclough/poll4pop). The latfordisp.R, kerncalc.R, and growth.func.R functions are identical copies from poll4pop.
- For latest versions and guidance, contact the corresponding author: Emma Gardner (emmgar@ceh.ac.uk).