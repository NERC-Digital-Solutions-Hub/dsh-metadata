# Supporting information for the bird4pop model

## Overview
- Dataset contains the model code and parameter files required to run the bird4pop model, which simulates central-place foraging, dispersal, and population processes of UK passerine birds.
- Parameterised for three guilds (woodland specialist, woodland generalist, farmland passerine) and four representative species.
- Intended to support landscape-scale population simulations and decision-making in combination with other ecological information.

## Dataset contents
- Input parameters and model code:
  - InputParameters_v7, filename = bird_guild_params.csv
  - InputParameters_v7, filename = bird_habitat_params.csv
  - ModelCode, filename = run_bird4pop.R
  - ModelCode, filename = computeForageNesting_v3.R
  - ModelCode, filename = getsteadystatepop_v3.R
  - ModelCode, filename = runpop_bird_v3.R
  - ModelCode, filename = growth.func.R
  - ModelCode, filename = latfordisp.R
  - ModelCode, filename = kerncalc.R
- Supported inputs and resources:
  - Landscape raster (base landcover per pixel)
  - edgestack (edge feature rasters)
  - edgecodes (landcover code for each edge feature)
  - guilds (names of bird guilds to simulate)
  - fol_c (path to R scripts directory)
  - fol_ip (path to input parameter files directory)
- Outputs (per simulated guild):
  - Nesting resources
  - Breeding season foraging resources
  - Number of adult pairs (current breeding season)
  - Number of offspring fledged
  - Adults surviving after yearly mortality
  - Offspring surviving after yearly mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing up surviving birds
  - Adult pairs available after nest-site limitation
  - Foraging rate per pixel (breeding season)
  - Foraging resources gathered per pixel
  - Nest site locations

## Inputs and data structures
- Landscape input:
  - Raster of base landcover per pixel; landcover codes must match bird_habitat_params.csv
  - Recommended minimum landscape size: 10 km x 10 km
  - Pixel wrap-around (toroidal); include at least ~2 km buffer around study area to avoid edge effects
- Parameters files:
  - bird_guild_params.csv: columns include
    - guild_names, guild, growthparam_a, growthparam_b, range_breeding_m, range_dispersal_m
    - maxnestdensity_perha, chicksperyear_mean, survprob_adult, survprob_juv
  - bird_habitat_params.csv: columns include
    - guild, Code_ExpOp, nesting (0-1 scale), nesting_se, nesting_alpha, nesting_beta
    - foraging_P1 (0-5 scale), foraging_P1_se, foraging_P1_alpha, foraging_P1_beta
  - These parameters were derived from expert opinion (nesting vs foraging resources) and literature sources; mean nesting/foraging scores feed into density and resource calculations.
- Landcover coding:
  - Table of landcover codes (0–77) used to parameterise nest and forage resources; codes must align across landscape rasters and parameter files.
- Model inputs per the documentation:
  - The exact layout and columns are defined in the text sections 2.1–2.4 and Table 1.

## Model code and processing workflow
- Top-level execution:
  - run_bird4pop.R orchestrates the simulation using computeForageNesting_v3.R, getsteadystatepop_v3.R, runpop_bird_v3.R, latfordisp.R, kerncalc.R, and growth.func.R
- Core functionality:
  - computeForageNesting_v3.R maps nesting and foraging resources across the landscape (minimally adapted from poll4pop’s computeFloralNesting.R)
  - getsteadystatepop_v3.R iterates yearly simulations via runpop_bird_v3.R until steady-state population
  - runpop_bird_v3.R simulates one-year processes: foraging, nest location, breeding pairs, offspring production, yearly survival, and dispersal
  - kerncalc.R computes the exponential kernels for central-place foraging and dispersal
  - latfordisp.R applies kernels to distribute foragers and dispersers according to resources and proximity
  - growth.func.R defines the population growth function (inverse logit) to determine offspring per pixel
- Reproducibility and lineage:
  - Several components are copied from the poll4pop model (links provided)
  - The dataset includes versioned parameter files (e.g., InputParameters_v7) and reference to latest versions for updates

## Parameterisation and data sources
- Nesting and foraging resource parameters (2.1):
  - Derived from expert opinion (n=4) across 77 landcover types
  - Scaled nesting scores to 0-1; foraging scores retained on 0-5
  - Means and beta-distribution parameters provided to enable uncertainty analyses; beta draws must be scaled for foraging (multiply by 6) when using the 0-5 scale
- Dispersal, survival, and chick production (2.2–2.4):
  - Dispersal ranges from Paradis et al. (1998)
  - Survival probabilities and mean chicks per year from Robinson (2005)
  - Maximum nest density derived from Batten (1976) data; applied as a mean across guilds (approximately 5 nests ha-1) for simplicity
  - Foraging range (250 m) and growth parameter a (0.2) chosen to match occupancy and resource limitation patterns; growth parameter b set to 2a
- Species and guild composition (2.4):
  - Guilds: woodland specialist, woodland generalist, farmland passerine
  - Four representative species linked to guilds for validation and parameter context (nuthatch, robin, yellowhammer, skylark)

## Validation
- Validation approach:
  - Bird4pop run across Great Britain (10x10 km or 10x10 m scale in validation) compared to Breeding Bird Survey (BBS) data from 2016–2020
  - For each 1x1 km survey square, observed maximum counts used as index of relative abundance; model-predicted breeding pairs compared via a Poisson GLM: ln(Ai) = β0 + β1 Bi
- Key results:
  - Woodland specialist: strong positive relationship (β1 ≈ 93.2; R2 ≈ 0.365)
  - Woodland generalist: positive relationship (β1 ≈ 36.5; R2 ≈ 0.165)
  - Farmland passerine: positive relationship (β1 ≈ 15.8; R2 ≈ 0.010)
  - Species-specific notes provided (nuthatch, robin, yellowhammer, skylark) with corresponding coefficients
- Interpretation:
  - Model captures broad-scale relative abundance patterns, with stronger fit for woodland guilds than farmland passerines, supporting utility for landscape-scale decision contexts

## Outputs
- Per simulated guild, the model outputs rasters with equal extent/resolution to the input landcover raster:
  - Nesting resources
  - Breeding season foraging resources
  - Number of adult pairs in current breeding season
  - Number of offspring fledged
  - Adults surviving after mortality
  - Offspring surviving after mortality
  - Total surviving birds after dispersal
  - Adult pairs after pairing up surviving birds
  - Adult pairs available for next breeding season after nest-site limitations
  - Foraging rate per pixel during breeding season
  - Foraging resources gathered per pixel
  - Nest site locations

## Role in decision-making
- Designed to support decision-makers alongside other ecological information (field surveys, local knowledge)
- Not intended to drive decisions in isolation; outputs should be interpreted with awareness of input uncertainties and local context

## Data governance and stewardship considerations
- Provenance and authorship:
  - Emma Gardner (corresponding author), UK Centre for Ecology and Hydrology; co-authors listed
  - Affiliations: CEH, British Trust for Ornithology
- Versioning and updates:
  - Example parameter file set is InputParameters_v7; model description notes ongoing improvements and guidance via contact before use
  - Reliance on latest versions recommended; references to poll4pop components and Zenodo DOI for broader model family
- Accessibility and reproducibility:
  - Model is modular with clearly defined input files, parameter columns, and R scripts
  - Documentation specifies input formats, landcover coding, and required fields to ensure standardised use
- Data quality and limitations:
  - Expert-derived resource parameters with quantified uncertainty (beta distributions) to enable uncertainty quantification
  - Validation indicates varying goodness-of-fit by guild; results should inform, not replace, ground-truth data
- Practical considerations for data management:
  - Large landscape rasters and multiple dependency scripts require sufficient storage and compute resources
  - Edge effects and toroidal landscape handling require careful buffering when applying to real study areas
  - Ensuring landcover codes align across input landscape and parameter files is essential for reproducibility

## Access, contact, and references
- Latest versions and guidance: contact Emma Gardner (emmgar@ceh.ac.uk)
- Key references and links:
  - poll4pop model components and code (GitHub and Zenodo links referenced in documentation)
  - Gardner et al. (2024) Landscape Ecology: family of process-based models
  - Supporting methodological references (e.g., Paradis 1998; Robinson 2005; Batten 1976; Hinsley et al. 1996)
- Acknowledgements: thanks to Breeding Bird Survey volunteers and contributing researchers