# Supporting information for the bird4pop model

- The bird4pop model is a process-based tool that simulates central-place optimal foraging, nest dispersal, and population dynamics of UK passerine birds across a landscape, iterating to a steady-state carrying capacity. It supports three guilds (woodland specialist, woodland generalist, farmland passerine) and four representative species.

## Data files, code and structure included

- The dataset provides both model code and input parameter files necessary to run bird4pop:
  - Input parameters and habitat/resource mappings:
    - InputParameters_v7, bird_guild_params.csv
    - InputParameters_v7, bird_habitat_params.csv
  - Model code (R scripts):
    - run_bird4pop.R (top-level)
    - computeForageNesting_v3.R
    - getsteadystatepop_v3.R
    - runpop_bird_v3.R
    - growth.func.R
    - latfordisp.R
    - kerncalc.R
- These files enable mapping resources, simulating foraging and nesting, dispersal, and population dynamics, with explicit sections describing their roles and how they interconnect.

## Model description (high level)

- Purpose: simulate central-place foraging around nests during the breeding season; offspring production depends on forage resources; adults and offspring disperse; populations are iterated year-to-year to reach steady state.
- Key processes:
  - Resource mapping: creates nesting resources and breeding-season foraging resources maps from landscape data and guild-specific parameters; handles multi-landcover pixels via area-weighted sums.
  - Nest placement: random Poisson allocation across landscape based on nesting resource map.
  - Foraging: Fourier transform-based convolution of foragers at nests with the foraging resource map, producing a foraging-rate per pixel and estimated resource gathering.
  - Productivity: nest productivity linked to foraging via a log-normal relationship (parameters a and b).
  - Survival: separate adult and offspring survival probabilities applied year-to-year (binomial sampling).
  - Dispersal: surviving birds disperse using a kernel-weighted process anchored to nesting resources; dispersal uses Fourier-based distance kernels.
  - Pairing: survivors are re-paired into breeding pairs, capped by nest density per pixel, then the next breeding season begins.
  - Iteration: repeats until landscape-wide population size stabilizes; final nest distribution reflects resource and dispersal constraints.
- Outputs per simulated guild:
  - Nesting resources, breeding-season foraging resources
  - Number of adult pairs current season
  - Number of offspring fledged
  - Survivors (adults and juveniles) after yearly mortality
  - Total survivors after dispersal
  - Post-pairing and post-nest-limitation breeding-pair counts
  - Foraging-rate per pixel and resources gathered per pixel
  - Nest site locations

## Input data requirements

- Landscape input
  - A raster of base landcover; codes must match bird_habitat_params.csv
  - Recommended minimum landscape size: 10 km x 10 km
  - Landscape wrapping: edges wrap around (toroidal)
  - Buffers: include at least a 2 km buffer around area of interest to mitigate edge effects
- Spatial and parameter inputs
  - cellsize: meters per pixel
  - edgestack: rasters for edge features (e.g., hedgerows) with corresponding edgecodes
  - edgecodes: landcover codes for each edge feature
  - guilds: names of bird guilds to simulate (must match bird_guild_params.csv)
  - fol_c: directory path to model code scripts
  - fol_ip: directory path to input parameter files
- bird_guild_params.csv (required columns)
  - guild_names, guild, growthparam_a, growthparam_b
  - range_breeding_m, range_dispersal_m, maxnestdensity_perha
  - chicksperyear_mean, survprob_adult, survprob_juv
- bird_habitat_params.csv (required columns)
  - guild, Code_ExpOp (landcover code, matches landscape and edgecodes)
  - nesting (0-1; with optional nesting_se, nesting_alpha, nesting_beta)
  - foraging_P1 (0-5; with optional foraging_P1_se, foraging_P1_alpha, foraging_P1_beta)
- Notes on parameters
  - Means and beta-distribution parameters for habitat scores are provided to support uncertainty quantification; foraging scores are on a 0-5 scale and nesting scores are renormalised to 0-1.
  - For uncertainty runs, beta draws for mean habitat scores can be used; for foraging scores, draws must be scaled by 6 to map from 0-1 to 0-5.

## Model processes and data dependencies

- Resource mapping
  - Nesting resources: nesting attractiveness (0-1) × maximum nest density
  - Foraging resources: landcover-specific foraging scores (0-5)
  - Edge features: area-weighted combination within a pixel when multiple landcovers are present
- Foraging and dispersal kernels
  - Central-place foraging: distance-decay kernel applied to nest-based foragers
  - Dispersal: kernel applied to dispersers, weighted by nesting-resource availability
  - Kernels are calculated via kerncalc.R and applied by latfordisp.R
- Population dynamics
  - Productivity per nest tied to foraging via a log-normal relationship with parameters a and b (b = 2a)
  - Survival probabilities separate for adults and juveniles
  - Pairing and nest-site limitations impose constraints on breeding pairs per pixel
- Outputs are provided per guild, at the same resolution as the input landcover raster

## Parameterization and data sources

- Nesting and foraging resource parameters
  - Derived from expert opinion (n=4 experts) across 77 landcover types
  - Means and variances computed with certainty weighting; nesting scores renormalised to 0-1
  - Foraging scores preserved on a 0-5 scale; means and beta-distribution parameters included for uncertainty
- Dispersal, survival, and chick production
  - Dispersal ranges: abundance-weighted means from Paradis et al. (1998)
  - Survival probabilities and chicks per year: derived from Robinson (2005)
- Maximum nest density
  - Derived from Batten (1976) data; mean across three oakwood plots used
  - Applied uniformly across guilds for simplicity (to reflect landscape-use effects rather than species count)
- Foraging range and growth parameter calibration
  - Foraging range set to 250 m and growth parameter a = 0.2 for woodland specialists (scaled to other guilds)
  - Growth parameter b set to 2a
- Validation data
  - Spatial validation against 2016-2020 Breeding Bird Survey (BBS) data across Great Britain
  - Generalized linear model (Poisson) links predicted breeding pairs to observed relative abundance; significant positive relationships reported for all guilds/species

## Model validation and interpretation

- Validation approach
  - Predictions of breeding-pair abundance compared to BBS-derived abundance indices
  - Reported significant positive relationships between predicted and observed abundances
- Caveats for decision-making
  - Outputs are intended to support, not replace, on-the-ground data and local ecological knowledge
  - Results should be interpreted with caution given input uncertainties and model assumptions

## Outputs and how to use them (data products)

- Generated rasters for each simulated guild, including:
  - Nesting resources and breeding-season foraging resources
  - Number of adult pairs, offspring produced, and survivors (adult/juvenile) per year
  - Total survivors after dispersal and post-dispersal breeding-pair counts
  - Foraging rate per pixel and total resources gathered per pixel
  - Nest site locations
- Use cases (data support perspective)
  - Inform landscape-scale planning and management by identifying regions with high nest/resource potential
  - Support visualization dashboards (self-serve data products) showing habitat/resource suitability
  - Enable scenario testing by varying habitat parameters or landscape configurations
  - Combine with survey data to validate or refine model assumptions and parameter estimates

## Outputs in decision support context

- Outputs are designed to complement field surveys and local knowledge; not to be used in isolation for policy decisions
- Provides spatially explicit indicators of carrying capacity and potential population dynamics under landscape scenarios

## Accessibility and reproducibility

- Model is parameterized for three guilds and four representative species, with inputs and parameters designed for transparency and repeatability
- Script and parameter dependencies are documented, and the model codebase references freely available components (poll4pop) for certain functions
- Corresponding author contact for latest versions and guidance: emmgar@ceh.ac.uk

## Acknowledgements and references (selected)

- Validation data from the Breeding Bird Survey (BBS) and contributions from UK CEH and BTO/BBRO teams
- Key references informing parameterization and model structure (e.g., Hinsley et al. 1996; Paradis et al. 1998; Robinson 2005; Gardner et al. 2020, 2024)