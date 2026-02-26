# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UKSSPs) and climate projections (UK-RCPs)

## Overview
- Projection dataset describing future land use in Great Britain at 1 km resolution.
- Based on an agent-based model (CRAFTY-GB) driven by linked UK-RCP climate scenarios and UK-SSP socio-economic pathways.
- Decadal timesteps from 2020 to 2080 across six SSP-RCP scenario combinations.
- Outputs include gridded land-use maps with seven bands per raster (one per decade) and an index-based representation of land-use agents.

## Data Access and Citation
- Data available at: https://doi.org/10.5285/f9ab3051-4f85-415f-b691-371ff8e951f2
- Licence: Open Government Licence.
- Citation required: Brown, C.; Seo, B.; Alexander, P.; et al. (2023). Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs). NERC Environmental Information Data Centre (Dataset).

## Data Structure and Scope
- Six SSP-RCP scenario combinations are provided for Great Britain: RCP2.6-SSP1, RCP4.5-SSP2, RCP4.5-SSP4, RCP6.0-SSP3, RCP8.5-SSP2, RCP8.5-SSP5.
- For each scenario, data are 1 km gridded land-use maps, stored as stacked rasters with seven bands (2020, 2030, 2040, 2050, 2060, 2070, 2080).
- Land Use Agents are encoded as indices from -1 to 15, with a provided mapping to agent names (e.g., Unmanaged, Agroforestry, Bioenergy, Intensive arable, Urban, etc.).
- The model accounts for global change through a broader LandSyMM framework, but is constrained to Great Britain due to data limitations for Northern Ireland.

## Land Use Agents and Values
- Agents represent main land-use forms across three domains:
  - Arable: Intensive arable (food), Intensive arable (fodder), Sustainable arable, Extensive arable.
  - Pasture: Intensive pastoral, Extensive pastoral, Very extensive pastoral.
  - Forest: Productive native conifer, Productive non-native conifer, Productive native broadleaf, Productive non-native broadleaf, Multifunctional mixed woodland, Native woodland (conservation).
  - Combined: Bioenergy, Agroforestry.
  - Unmanaged and Urban are also represented.
- Each agent type corresponds to a set of ecosystem services (provisioning, regulating, cultural) and is associated with different production and management characteristics.

## Data Creation Methods
- Core inputs combine:
  - Capitals framework per 1 km2 cell: human, social, manufactured, financial, and natural capitals (with natural capital further divided into arable, pastoral, and forest yields/suitabilities).
  - Exogenous scenarios (climate and socio-economic) that influence capital values, agent characteristics, service demand/valuation, competition, and policy objectives.
- Data sources for capitals include eight UK-SSP indicators, ESC-based forest yields, and statistical models for arable/pastoral suitabilities.
- Protected areas (11 designation types and five private owners) constrain land-use change options and vary by SSP storyline.
- An urban component projects scenario-specific urban expansion via a separate urban model.

## Allocation and Initial Distribution of Land Uses
- Initial land-use distributions derived from:
  - LCM2015 (Land Cover Map) and National Forest Inventory (NFI) data (2010–2015).
  - Additional datasets for extent/location of specific land uses.
  - Unassigned areas treated as Unmanaged.
- Urban areas initialised from LCM2015 baseline and then projected via an urban allocation algorithm, using neighbourhood density, SSP-specific sprawl parameters, and protected areas/flood-risk exclusions.
- Coastal and island data gaps were addressed with regression or nearest-neighbour approaches; normalisation applied where 2020 inputs deviated from baselines.

## Intensity Representation in Outputs
- To aid interpretation, the model includes a continuous land-use intensity mapping across arable and pastoral classes (excluding very extensive pastoral).
- Intensity is a multiplicative combination of input use (fertilisers, pesticides, machinery), technology, and production levels.
- Intensity scalars are SSP-specific and provided to aid visual comparison across scenarios (Table 4 in the source).

## Model Components and Capitals
- Agent types and land uses are supported by a capital-based decision framework:
  - Capitals drive service production and influence competition among agents for each 1 km2 cell.
  - Protected areas and urban components constrain change options.
  - Ecosystem services include explicit categories (e.g., food crops, fodder, bioenergy, biodiversity, landscape diversity, carbon sequestration, recreation, flood regulation, employment).

## Climate and Socio-Economic Scenarios
- Climate: UK-RCPs provide decadal climate inputs up to 2080 (temperature, precipitation, evapotranspiration, growing degree days) used by crop, grassland, and forest modules.
- Socio-economics: UK-SSPs embed narratives and quantitative drivers (with stakeholder input) to shape demand, land-use decisions, and policy objectives.
- RCP-SSP combinations are chosen to span uncertainty and allow analysis of within-SSP and between-SSP differences as well as low vs high adaptation challenges.

## Model Evaluation and Validation
- Evaluation uses TRACE (TRAnsparent and Comprehensive model Evaluation) framework and includes:
  - Unit tests, sensitivity and uncertainty analyses.
  - Comparisons with empirical data and other models.
  - Documentation and open access to the model and outputs (e.g., landchange.earth/CRAFTY).
- Specific evaluation notes:
  - Not validated against historical UK land cover change due to data inconsistencies and lack of temporally consistent UK land-cover data.
  - Baseline agent-type allocations were compared with independent datasets to assess coverage and interpretation (LCM2015, EUNIS habitat map, CEH Land Cover Plus: Fertilisers and Pesticides).
- The evaluation supports the model’s appropriateness for exploring future land-use trajectories under UK-SSP and UK-RCP scenarios.

## Practical Implications for Environmental Monitoring Analysts
- Provides harmonised, decadal maps of potential future land uses under multiple climate-socioeconomic futures, enabling:
  - Monitoring of land-use transitions and pressures on ecosystems.
  - Assessment of policy performance related to land management, agriculture, forestry, and urbanization.
  - Cross-scenario analysis of ecosystem services provision, biodiversity, and carbon sequestration implications.
  - Integration with other monitoring data through standardised 1 km resolution outputs and clearly defined Land Use Agent indices.
- Useful as a decision-support resource for planning, conservation, and climate adaptation strategies, while acknowledging limitations such as the GB-wide scope (excluding Northern Ireland) and reliance on exogenous scenario inputs.