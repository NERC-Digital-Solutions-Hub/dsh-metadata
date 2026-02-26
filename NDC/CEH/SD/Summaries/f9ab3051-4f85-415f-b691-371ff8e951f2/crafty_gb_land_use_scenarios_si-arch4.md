# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs)

- Overview
  - Projections of future land use in Great Britain using the CRAFTY-GB agent-based land system model.
  - Combines six UK-RCP-SSP scenario pairs with decadal timesteps from 2020 to 2080 at 1 km2 resolution.
  - Outputs are gridded land-use maps and associated data to explore how climate and socio-economic changes shape the British land system.

- Data access and citation
  - Data available at: https://doi.org/10.5285/f9ab3051-4f85-415f-b691-371ff8e951f2
  - Licensed under the Open Government Licence; citation required:
    Brown et al. (2023). Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs). NERC Environmental Information Data Centre.

- Authors and affiliations
  - Multi-institutional team from KIT (Germany), University of Edinburgh, Forest Research, Lancaster, CEH, Oxford, Norwegian University of Life Sciences, Lancaster, and others.

- What the dataset describes
  - Future land-use projections produced by CRAFTY-GB, an agent-based model of the British land system.
  - Based on linked UK-RCP climate scenarios and UK-SSP socio-economic pathways, extrapolated to 2080 in decadal steps.
  - Embedded in a global modelling framework to account for global change and UK international trade; scope limited to Great Britain.

- Data structure and content
  - For each of the six SSP-RCP scenarios, 1 km gridded land-use maps are provided as stacked rasters with seven bands (one band per decadal timestep from 2020 to 2080).
  - Land-use representation uses Land Use Agent Indices from -1 to 15, mapped to specific land-use agent names (e.g., Unmanaged, Agroforestry, Bioenergy, various arable/pastoral/forest classes, Urban, etc.).
  - Includes components such as urban areas, protected areas, and ecosystems services (provisioning, regulating, cultural) linked to each land-use type.
  - Output includes a continuous Land Use Intensity mapping to better visualize management intensity across arable and pastoral classes (values reflect inputs, technology, and production levels).

- Data creation and inputs
  - Core model concept: land-cell capitals (human, social, manufactured, financial, natural) drive agent competition for land management based on service bundles and exogenous demand.
  - Capitals derived from UK-SSP projections and calibrated with observational data; natural capitals use site classification and yield/suitability models.
  - Agent types cover a wide range of land uses (intensive/extensive arable, intensive/extensive pastoral, various forest types, agroforestry, bioenergy, etc.) with continuous variation to reflect management gradients.
  - Initial land-use allocation uses baseline maps (LCM2015, NFI 2010-2015) and other data to place agent types; unmanaged areas cover remaining cells.
  - Urban areas are projected with a separate urban allocation model, downscaling from European-scale inputs and local authority projections (2020–2100).
  - Data processing to address gaps (coastal/island data, Shetland) and normalisation to ensure consistency with baselines.

- Model and scenario design
  - Six combined UK-RCP-SSP scenarios: RCP2.6-SSP1, RCP4.5-SSP2, RCP4.5-SSP4, RCP6.0-SSP3, RCP8.5-SSP2, RCP8.5-SSP5.
  - Scenarios chosen to cover uncertainty in emissions/climate and socio-economic development, including cross-SSP and cross-RCP comparisons.
  - Scenario-specific changes influence demand, capital values, agent behavior, and land-use policy objectives within the model.

- Output interpretation and intensity scalars
  - Outputs include a land-use intensity mapping (continuous values) to convey differences in management intensity across agro- and pastoral classes.
  - Intensity scalars provided per SSP for each decadal timestep (Table 4) to facilitate cross-scenario comparability.
  - Land Use Indices allow interpretation of the spatial distribution of land-use classes, with Urban treated separately.

- Data quality, evaluation, and limitations
  - Evaluation framework described in TRACE; includes unit tests, sensitivity analyses, comparisons with empirical data and other models, and open-access model tools (landchange.earth/CRAFTY).
  - Baseline agent-type allocation validated against multiple datasets:
    - Land Cover Map 2015 (LCM2015)
    - European EUNIS habitat classification
    - CEH Land Cover Plus: Fertilisers and Pesticides
  - Limitations:
    - GB-wide scope; data for Northern Ireland not available/consistent.
    - Coastal and island data gaps addressed with regression/nearest-neighbor methods; some residual uncertainty in those areas.
    - No attempt to reproduce historical UK land-use change due to data incompatibilities; model evaluated for representativeness rather than historical fit.
    - Some inputs required normalisation to align with baselines; urban projections rely on an independent urban model.

- Practical use and considerations for data leaders
  - Facilitates scenario planning and governance discussions around land-use futures under climate and socio-economic change.
  - Useful for assessing potential ecosystem-service outcomes, land-system resilience, and land-management policy implications under different UK pathways.
  - Provides a reproducible, open-access dataset with clear provenance, licensing, and citation guidelines to support transparency and collaboration.

- Access and usage notes
  - Data are openly licensed; users must cite the provided Brown et al. paper and dataset DOI.
  - Users can explore outputs via the referenced online tools (e.g., the CRAFTY platform) for interactive analysis and visualization.