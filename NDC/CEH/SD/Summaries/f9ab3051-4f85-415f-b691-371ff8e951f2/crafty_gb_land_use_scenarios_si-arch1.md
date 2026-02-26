# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs)

## Overview
- Presents decadal land-use projections for Great Britain (2020–2080) using the CRAFTY-GB agent-based model.
- Scales: 1 km grid; six combined UK-RCP-SSP scenarios, embedded in a global framework accounting for trade and global change.
- Outputs are gridded land-use maps (per decadal timestep) aligned with UK-RCP-SSP scenarios to explore potential future land-system change under climate and socio-economic drivers.

## Data content and format
- Data accessibility: available at the Open Government Licence dataset with DOI provided; citation required as Brown et al. (2023) NERC Environmental Information Data Centre.
- File structure: for each of six SSP-RCP scenarios, 1 km gridded land-use maps provided as a stacked raster with seven bands representing land use per decadal timestep (2020–2080).
- Land-use encoding: Land Use Agents are represented by indices from -1 to 15, mapping to names such as Unmanaged, Agroforestry, Bioenergy, various arable/pasture/forest classes, Urban, etc.
- Output interpretation: an intensity-mmapped representation was developed to aid interpretation, combining intensity of inputs, technology, and production levels; scalar values by SSP are provided to illustrate relative management intensity (Table 4 in the accompanying documentation).

## Model and scenarios
- Model framework: CRAFTY-GB, an agent-based model of the British land system, operating at 1 km resolution and driven by climate (UK-RCP) and socio-economic (UK-SSP) scenarios.
- Spatial footprint: limited to Great Britain (no Northern Ireland) due to data constraints, embedded within a global modelling framework to capture international trade and global change.
- Core components:
  - Capitals: human, social, manufactured, financial, and natural capitals (with natural capital further divided into yields/suitabilities for arable, pastoral, and forest uses).
  - Land-use agents: arable, pastoral, forest, and combined classes (e.g., bioenergy, agroforestry) representing a continuum of management intensity.
  - Services: provisioning, regulating, and cultural ecosystem services (e.g., food crops, fodder, bioenergy, biodiversity, carbon sequestration, recreation, flood regulation, employment).
  - Protected areas: constrain land-use change options.
  - Urban areas: projected via an independent urban-allocations model using SSP-specific sprawl and land-exclusion rules.
- Initialization and data sources:
  - Baseline land-use distributions initialized from LCM2015 and the National Forest Inventory (NFI 2010–2015).
  - Additional data layers define extent and location of land uses; some gaps are filled via regression or nearest-neighbor approaches.
  - Urban projections derived from a two-step process: downscaling European-scale projections and then downscaling LAD-level UK-SSP population projections to urban land.
- Scenario design:
  - Six RCP-SSP combinations: RCP2.6-SSP1, RCP4.5-SSP2, RCP4.5-SSP4, RCP6.0-SSP3, RCP8.5-SSP2, RCP8.5-SSP5.
  - Each combination calibrates model parameters and determines which processes are active, enabling analysis of climate and socio-economic effects on land-use outcomes.
  - UK-SSP narratives and quantitative inputs are integrated with a global LandSyMM framework for cross-sector consistency.

## Data structure and components
- Capitals, ecosystems, and protection:
  - Capitals: human, social, manufactured, financial, natural (arable, pastoral, forest yields/suitabilities).
  - Ecosystem services: a broad set including crops, fodder, bioenergy, timber, biodiversity, landscape diversity, carbon, recreation, and more.
  - Protected areas: 11 designation types plus private land owners, affecting change feasibility.
- Agent types and land-use allocation:
  - Agent types span intensive and extensive arable, intensive/extensive pastoral, very-extensive pastoral, productive native/non-native conifers and broadleaf forests, multifunctional woodland, native woodland for conservation, agroforestry, and bioenergy.
  - Initial distribution allocated according to LCM2015, NFI, and related datasets; unmanaged areas assigned where no suitable use is defined.
- Urban areas:
  - Projections derived from a dedicated urban allocation algorithm using neighbourhood density, SSP-spread parameters, and land exclusions (flood risk, protected areas).
- Climate and socio-economic drivers:
  - Climate inputs: UKCP18-derived climate variables (temperature, precipitation, evapotranspiration, growing degree days) at 1 km resolution.
  - Socio-economic inputs: UK-SSP narratives and indicators, aligned with a global-consistent framework and stakeholder-informed drivers.
- Model outputs and visualization:
  - Land-use intensity mapping: continuous values to convey management intensity across arable and most pastoral classes (except very extensive pastoral) to enhance interpretability in maps.
  - Intensity scalars (Table 4) provide SSP-specific multipliers to illustrate changes in input use, technology, and production levels over time.

## Model evaluation and validation
- Evaluation approach: TRACE-based evaluation documented in Supporting Information S2; includes unit tests, sensitivity and uncertainty analyses, and comparisons to empirical data and other models.
- Validation scope:
  - Model structure and outputs evaluated against literature and expert input; full historical reproduction validation not performed due to lack of consistent UK land-cover time-series data across all classes.
  - Baseline agent distributions compared to independent datasets (LCM2015, EUNIS habitat classifications, CEH Land Cover Plus Fertilisers and Pesticides) to assess representativeness and coverage of land-use and ecological characteristics.
- transparency and accessibility: comprehensive model documentation and open-access tools (e.g., landchange.earth/CRAFTY) with detailed descriptions of model design and evaluation.

## Usage notes and citations
- Data access and citation:
  - Primary dataset: Brown, C.; Seo, B.; Alexander, P.; et al. 2023. Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs). NERC Environmental Information Data Centre. Dataset. DOI provided in the dataset page.
  - Data licensed under the Open Government Licence.
- Related literature and technical references:
  - Foundational papers on CRAFTY-GB model design, calibration, and evaluation.
  - Supporting information references detailing capitals, services, scenario details, urban allocation, and intensity mapping.

## Key takeaways for analysts
- This dataset provides 1 km resolution decadal projections (2020–2080) of land-use changes in Great Britain under six UK-RCP-SSP futures, using a mechanistic agent-based framework (CRAFTY-GB) that links climate, socio-economics, and land-management decisions.
- Outputs include a consistent set of scenario-specific land-use maps with detailed taxonomies of land-use agents, protected areas, urban extension, and ecosystem-service implications.
- The data are suitable for assessing how different climate and socio-economic trajectories may reshape land-use intensity, biodiversity, carbon dynamics, and provisioning/regulating services across Great Britain, with explicit caveats about Northern Ireland exclusion and historical validation limitations.
- Analysts should integrate the intensity-mapping approach and SSP scalars when comparing scenario results, and consult the Supporting Information for methodological details, calibration, and evaluation procedures.