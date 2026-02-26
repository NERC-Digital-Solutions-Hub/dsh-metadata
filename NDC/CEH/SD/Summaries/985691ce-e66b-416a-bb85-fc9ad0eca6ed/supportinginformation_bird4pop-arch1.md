# Supporting information for the bird4pop model

- This document accompanies the bird4pop model, including the data inputs, parameterisations, and validation approaches used to simulate UK passerine population dynamics and landscape use.

## 1. Model description

- Bird4pop simulates central-place optimal foraging of nidicolous birds around nests during the breeding season. Offspring numbers depend on forage resources and the landscape’s carrying capacity.
- Processes include: nest-site selection, central-place foraging, dispersal, survival (separate adult and juvenile survival), pairing, and multi-year iteration to the landscape’s steady-state carrying capacity.
- Model supports three guilds (woodland specialist, woodland generalist, edge-nesting farmland passerines) and four representative species.
- Core computational flow:
  - Decompose landscape into nesting resources map and breeding-season foraging resources map.
  - Randomly allocate initial nest sites per pixel (Poisson around expected nests) and assign breeding pairs.
  - Foraging: use Fourier transforms to convolve nest locations with the foraging resources map via a distance-decay kernel.
  - Population growth: productivity per nest related to foraging resources via a log-normal CDF (median a; variance b = 2a).
  - Post-season survival via binomial draws (separate adult and juvenile survival).
  - Dispersal: survivors dispersed using a kernel weighted by nesting resources; dispersers are pooled into breeding pairs with a 50:50 sex ratio and nest-site limits per pixel.
  - Iterate across years until steady-state population size is reached. Final nests persist where resources suffice or dispersal brings individuals within productive areas.
- Outputs reflect multiple facets of population and resource use and include carrying capacity conditions driven by nesting vs foraging resources.
- Role in decision-making: intended to support, not replace, land-management decisions; outputs should be considered with other ecological information and local knowledge.

## 1.1 Short summary

- Central-place foraging model for UK passerines; combines nesting and foraging resources with dispersal, survival, and population growth to determine steady-state landscape carrying capacity.
- Distinguishes adult and juvenile survival; iterates to equilibrium; produces spatially explicit rasters of resource and population metrics.

## 1.2 Detailed description of computational processes

- Landscape decomposition:
  - Nesting resources map: nesting attractiveness (0–1) × maximum nest density per guild.
  - Foraging resources map: breeding-season foraging resources (0–5) per landcover/ guild.
  - When multiple landcovers occupy a pixel, area-weighted sums yield pixel resource values, including edge features (hedgerows, margins) via edgestack rasters.
- Initialization: random nest placement per pixel around expected nests; each nest forms a breeding pair.
- Foraging convolution: Fourier transform-based convolution of nest-occupying foragers with the foraging resources map, yielding per-pixel foraging rates and resources gathered.
- Productivity and growth: nest productivity linked to foraging via a log-normal CDF with median a and variance b = 2a.
- Survival: separate adult and juvenile yearly survival probabilities, applied to determine survivors for next year.
- Dispersal and re-pairing: surviving birds disperse using a nesting-resource-weighted distance-decay kernel; arriving dispersers form breeding pairs, limited by available nests.
- Iteration: repeat breeding-season dynamics with surviving birds as breeders until steady state; final nest distribution reflects resource availability and dispersal reach.
- Inputs required:
  - Landscape raster (base landcover; square extents; matching codes to bird_habitat_params.csv).
  - cellsize (meters), edgestack and edgecodes (edge features within pixels), guilds (names matching bird_guild_params.csv), fol_c (model scripts), fol_ip (input parameter files).
  - bird_guild_params.csv: guild_names, guild (code), growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m, maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv.
  - bird_habitat_params.csv: guild, Code_ExpOp (landcover code), nesting (0–1), nesting_se, nesting_alpha, nesting_beta, foraging_P1 (0–5), foraging_P1_se, foraging_P1_alpha, foraging_P1_beta.

## 1.3 Model inputs and files

- Input parameter files:
  - bird_guild_params.csv and bird_habitat_params.csv containing guild-level and habitat-level parameters (including survival, fecundity, nest density, foraging resources, and movement ranges).
- Landscape and edge data:
  - landscape raster (base landcover codes per pixel; 10 km × 10 km recommended minimum)
  - cellsize in meters
  - edgestack rasters (edge feature areas per pixel)
  - edgecodes vector (mapping edgestack to landcover codes)
- Model scripts and code:
  - run_bird4pop.R (top-level)
  - computeForageNesting_v3.R (maps nest and forage resources)
  - getsteadystatepop_v3.R (iterates until steady state)
  - runpop_bird_v3.R (annual foraging and population dynamics)
  - growth.func.R (population growth function)
  - latfordisp.R (dispersal and foraging distribution)
  - kerncalc.R (distance-decay kernel calculations)

- Note: computeForageNesting_v3.R is adapted from computeFloralNesting.R (poll4pop model), and several functions latfordisp.R, kerncalc.R, and growth.func.R are identical copies from poll4pop.

## 1.4 Parameterisation and data sources

- 2.1 Nesting and foraging resource parameters: expert opinion (n=4 experts) used to rate 77 landcover types on nesting (0–1) and foraging (0–5) per guild; scores averaged and uncertainty quantified by beta distributions (parameters included in bird_habitat_params.csv). Mean nesting scores renormalised to 0–1; foraging scores retained 0–5 scale.
- 2.2 Dispersal, survival and chick production: dispersal ranges from Paradis et al. (1998); survival probabilities and mean chicks per year derived from Robinson (2005); species lists per guild provided in Table 2.
- 2.3 Maximum nest density: derived from Batten (1976) data; mean across three oakwood plots used to derive Dperspecies = 0.687 ha−1 species−1; with Nspecies per guild (9 for woodland specialist, 10 for woodland generalist, 5 for farmland passerine) leading to D ≈ 5 nests ha−1 on average. For simplicity, uniform nest density applied across guilds to focus on habitat-use differences rather than species-count differences.
- 2.4 Foraging range and population growth: calibration for woodland specialists using Hinsley et al. (1996); chosen foraging range 250 m and growth parameter a = 0.2; growth parameter b set to 2a = 0.4; applied to all guilds to preserve proportional resource-to-chick conversion and due to limited species-specific estimates.

- Validation and calibration notes:
  - Foraging range and growth parameters chosen to align with occupancy and resource-limited vs. patch-size-dependent dynamics.
  - Beta-distributed uncertainty allows repeated runs to explore parameter uncertainty (note: foraging beta draws must be scaled appropriately; see methods in habitat parameter file).

## 2. Model validation

- Validation dataset: Breeding Bird Survey (BBS) 2016–2020, across Great Britain (n = 4,874 survey squares).
- Method: for each square and year, use the maximum observed count per visit, average over five years to obtain Ai (observed relative abundance); compare with Bi (predicted mean breeding pairs from bird4pop) using a Poisson GLM: ln(Ai) = β0 + β1 Bi.
- Outcome: Significant positive relationship between predicted breeding pairs and observed abundance for all guilds and species parameterisations.
- Representative results (illustrative coefficients; unitless):
  - Woodland specialist: β1 ≈ 93.2; R2 ≈ 0.365
  - Woodland generalist: β1 ≈ 36.5; R2 ≈ 0.165
  - Farmland passerine: β1 ≈ 15.8; R2 ≈ 0.010
  - Species-level validations (e.g., Nuthatch, Robin, Yellowhammer, Skylark) support positive associations, with varying strength.

## 3. Outputs

- For each simulated guild, rasters with the same extent/resolution as input landscape:
  - Nesting resources
  - Breeding-season foraging resources
  - Number of adult pairs in current breeding season
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Offspring surviving after yearly mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing up surviving birds (pre-nest limitation)
  - Adult pairs available to start next breeding season after nest limitation
  - Foraging rate per pixel during breeding season
  - Foraging resources gathered into each pixel during breeding season
  - Nest site locations

## 4. Acknowledgements

- Acknowledges voluntary Breeding Bird Survey contributors and related data providers.

## 5. References

- Key sources informing parameter choices, dispersal, survival, habitat resources, and model calibration include:
  - Hinsley et al. (1996)
  - Batten (1976)
  - Paradis et al. (1998)
  - Robinson (2005)
  - Gardner et al. (2020, 2024)
  - Häussler et al. (2017)
  - Newson et al. (2009)
  - Eaton & Noble (2021)
  - Pollination-related model references (poll4pop) for code provenance

- Additional notes:
  - The model is designed to be updated with newer versions; refer to the corresponding corresponding author for latest versions and guidance.