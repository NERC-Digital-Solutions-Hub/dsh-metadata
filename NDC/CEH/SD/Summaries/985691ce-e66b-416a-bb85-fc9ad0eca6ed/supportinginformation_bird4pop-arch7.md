# Supporting information for the bird4pop model

- Purpose: A dataset and accompanying code that enable running the bird4pop model, which simulates central-place foraging, nest provisioning, dispersal, and population dynamics of UK passerine birds across landscapes. It includes model code, input parameter files, and documentation for running and interpreting the model outputs.

- Core authors and affiliations: Emma Gardner et al. from UK Centre for Ecology and Hydrology and British Trust for Ornithology; correspondence with Emma Gardner.

- Scope of outputs: Per simulated bird guild, a suite of raster outputs at the same resolution and extent as the input landcover raster, describing resources, population processes, and dispersal, plus nest site locations.

- Intended use: To support decision-makers alongside other ecological information. Outputs should not be used in isolation for decision-making.

Data inputs and GIS requirements

- Landscape input: A single raster denoting base landcover per pixel, with codes matching those used in bird_habitat_params.csv; landscape extents must be square or rectangular with square pixels. Wrapped (toroidal) edges for computation, so edge effects can be mitigated by including a buffer around the area of interest (recommended at least 2 km).

- Spatial parameters:
  - cellsize: pixel size in meters (e.g., 10 m).
  - edgestack: stack of edge feature rasters (same extent/resolution as landscape) denoting area within each pixel covered by edge features (in m2).
  - edgecodes: landcover codes corresponding to each edge feature in edgestack.

- Guild configuration:
  - guilds: vector of bird guild names to simulate; each guild must have corresponding habitat parameters in bird_habitat_params.csv.

- Model scripts and inputs directory structure:
  - fol_c: path to directory containing core R scripts (computeForageNesting_v3.R, getsteadystatepop_v3.R, runpop_bird_v3.R, kerncalc.R, latfordisp.R, growth.func.R).
  - fol_ip: path to directory containing input parameter files (bird_guild_params.csv, bird_habitat_params.csv).

- Input parameter files:
  - bird_guild_params.csv: columns include guild_names, guild, growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m, maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv, among potentially additional uncertainty fields.
  - bird_habitat_params.csv: columns include guild, Code_ExpOp (landcover code), nesting (0-1 scale), nesting_se, nesting_alpha, nesting_beta, foraging_P1 (0-5 scale), foraging_P1_se, foraging_P1_alpha, foraging_P1_beta; these map habitat types to nesting and foraging resource scores for each guild.

- Representative species and guilds: The model parameterisation covers three guilds (woodland specialist, woodland generalist, farmland passerine) and four exemplar species (nuthatch, robin, yellowhammer, skylark) used for validation and demonstration, with parameters derived from literature and expert opinion.

- Landcover codes: A fixed coding system (Table 1 in the document) that links landscape codes to habitat categories used by the model, including various woodland types, edge features, water features, grassland types, arable crops, urban types, etc.

Computational processes (model workflow)

- Resource mapping:
  - Nesting resources per landcover are calculated by multiplying nesting scores (0-1) by maximum nest density per hectare.
  - Foraging resources per landcover are mapped to breeding season foraging scores (0-5 scale).
  - If pixels contain multiple landcovers (including edge features), resource values are area-weighted sums of component landcovers.

- Initialization:
  - Nest sites are randomly allocated across the landscape; per-pixel nest counts follow a Poisson distribution around expected nests from the nesting resources map; each nest is assigned a breeding pair.

- Foraging approximation:
  - A Fourier transform-based convolution of nest-based foragers with the foraging resources map, using a distance-decay kernel parameterised by the foraging distance.
  - This yields foraging rates per pixel and estimates how much foraging resources foragers gather from their surroundings.

- Population growth:
  - Productivity at each nest (offspring per year) is linked to available foraging resources via a log-normal cumulative distribution function (median a, variance b=2a).

- Survival and dispersal:
  - End-of-year survival is determined by binomial draws with separate adult and juvenile survival probabilities.
  - Surviving individuals disperse by convolving dispersers with the nesting resources map, using a central-place distance-decay kernel weighted by dispersal distance.
  - Arriving dispersers are condensed into breeding pairs (50:50 sex ratio) and constrained so breeding pairs per pixel do not exceed the pixel’s nest density capacity.

- Iteration to steady state:
  - The process repeats year-by-year using survivors as the breeding population until a landscape-wide carrying capacity (steady-state population size) is reached.
  - Final nest distribution persists only where resources sustain nests or where dispersal brings visitors to more productive areas.

- Outputs per guild (rasters, same extent/resolution as input landscape):
  - Nesting resources
  - Breeding season foraging resources
  - Number of adult pairs in current breeding season
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Juveniles surviving after yearly mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing up surviving birds (before nest-site limitation)
  - Adult pairs available for next breeding season after nest-site limitation
  - Foraging rate per pixel during breeding season
  - Foraging resources gathered per pixel during breeding season
  - Nest site locations

Model parameterisation and validation (how inputs were set)

- Resource parameters (nesting and foraging) by landcover:
  - Derived from expert-opinion questionnaires (n=4 experts) across 77 landcover types, with scores scaled to nesting (0-1) and foraging (0-5).
  - Means and uncertainties (beta-distribution parameters) are provided in bird_habitat_params.csv for use in uncertainty analyses; foraging scores drawn from beta distributions should be scaled by six to translate to the 0-5 foraging scale.

- Nest density parameter:
  - Maximum nest density derived from Batten (1976) data on oakwood plots; mean per-guild density approximated to 5 nests per hectare for simplicity, applying the same mean density across all guilds.

- Foraging range and growth parameters:
  - For woodland specialists: foraging range set at 250 m; growth parameter a = 0.2; growth parameter b = 2a.
  - These values produce a balance between nest-resource limitation and forage-resource limitation across typical patch sizes, and are applied across guilds for comparability.

- Dispersal, survival, and chick production:
  - Dispersal distances and survival parameters drawn from literature (Paradis et al. 1998; Robinson 2005) with adult and juvenile survival treated separately.

Model validation

- Validation dataset: Great Britain-wide comparison against Breeding Bird Survey (BBS) data for 2016–2020 (n ≈ 4,874 squares).
- Method: For each 1x1 km BBS square, observed relative abundance is regressed against predicted breeding-pair density from bird4pop using a Poisson GLM on the log scale.
- Outcome: Significant positive relationships between modeled breeding pairs and observed abundance across guilds and species (e.g., woodland specialist, woodland generalist, farmland passerine; table of coefficients with strong significance).

Code and dependencies (what to run)

- Top-level model runner:
  - run_bird4pop.R: orchestrates the simulation for specified landscape, guild(s), and parameters.

- Core computational components (each accomplishes a specific task in the workflow and are invoked by run_bird4pop.R):
  - computeForageNesting_v3.R: maps nesting and foraging resources across the landscape (adapted from poll4pop’s computeFloralNesting.R).
  - getsteadystatepop_v3.R: iterates population dynamics until steady state is reached by repeatedly calling runpop_bird_v3.R.
  - runpop_bird_v3.R: simulates yearly foraging and population processes for a given landscape/资源 field.
  - kerncalc.R: computes exponential kernels for central-place foraging and dispersal; used twice in the workflow.
  - latfordisp.R: applies spatial kernels to allocate foragers and dispersers across the landscape; used twice (for foraging distribution and post-dispersal distribution).
  - growth.func.R: defines the inverse-logit-based growth function to determine offspring production per pixel.

- External references and copies:
  - Some components are based on the poll4pop model; related code is available at GitHub (https://github.com/yclough/poll4pop, DOI Zenodo 4001015).

- Outputs, visualization, and usage:
  - Outputs are raster layers aligned to the input landscape’s extent and resolution, enabling direct GIS integration and visualization.
  - The dataset emphasizes map-based data products suitable for informing policy colleagues, clients, and the public, while acknowledging uncertainty and the need for caution in decision-making.

Notes for GIS deployment

- Edge handling and buffering: The model uses edge wrapping during computation; include a buffer around the area of interest to avoid edge effects in results.
- Resolution and reprojection: Ensure the input landscape raster and edge feature rasters are co-registered at the same resolution and projection to avoid misalignment in the convolution/dispersal steps.
- Resource scaling: Nesting and foraging resource scores, and their beta-distribution parameters, feed directly into landscape-wide maps of habitat suitability and population potential; uncertainty can be explored by sampling from the provided distributions.
- Validation and interpretation: Use the provided validation results as a benchmark, but consider local survey data and land-management context for region-specific interpretation.

Acknowledgements and references (highlights)

- Validation data from the Breeding Bird Survey (BBS) coordinated by BTO/RSPB/JNCC.
- Foundational literature spanning Hinsley et al. (1996), Paradis et al. (1998), Robinson (2005), and Gardner et al. (2020, 2024), among others, informing model structure, parameters, and interpretation.
- The model build integrates expert opinion on habitat resources (nesting vs foraging) across landcover types to parameterize habitat scores and uncertainties.