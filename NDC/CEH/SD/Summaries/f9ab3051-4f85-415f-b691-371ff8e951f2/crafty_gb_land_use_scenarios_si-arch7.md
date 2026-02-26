# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UKSSPs) and climate projections (UK-RCPs)

## Access and citation
- Data available at https://doi.org/10.5285/f9ab3051-4f85-415f-b691-371ff8e951f2
- Open Government Licence; citation required: Brown et al. (2023) NERC Environmental Information Data Centre dataset
- Supporting documentation and details available in Brown et al. (2022) and related sources

## What the data are
- 1 km resolution gridded land-use projections for Great Britain, produced by the CRAFTY-GB agent-based model
- Decadal timesteps from 2020 to 2080
- Six UK-RCP-SSP scenario combinations (RCP2.6-SSP1, RCP4.5-SSP2, RCP4.5-SSP4, RCP6.0-SSP3, RCP8.5-SSP2, RCP8.5-SSP5)
- Embedded in a global modelling framework to account for global change and UK–international trade
- Urban areas projected with a separate urban allocation model

## Data structure and content
- For each of the six scenarios: a stacked 1 km raster with seven bands, representing land use at each decadal timestep (2020–2080)
- Land Use Agents encoded as indices from -1 to 15, with defined names (e.g., Unmanaged, Agroforestry, Bioenergy, Intensive arable, Urban, etc.)
- Key components described: capitals (human, social, manufactured, financial, natural), agent types, protected areas, urban areas, and ecosystem services
- Ecosystem services included: provisioning, regulating, cultural services (e.g., food crops, bioenergy, biodiversity, landscape diversity, carbon sequestration, recreation, flood regulation, employment)

## Land uses and agent types
- Agent types cover:
  - Arable: Intensive arable (food), Intensive arable (fodder), Sustainable arable, Extensive arable
  - Pastoral: Intensive pastoral, Extensive pastoral, Very extensive pastoral
  - Forest: Productive native conifer, Productive non-native conifer, Productive native broadleaf, Productive non-native broadleaf, Multifunctional mixed woodland, Native woodland (conservation)
  - Combined: Bioenergy, Agroforestry
- Allocation of initial land-use distribution based on LCM2015 and National Forest Inventory data; other inputs define extent/location of specific land uses
- Unmanaged areas represent margins where biophysical conditions limit productivity

## Urban areas
- Urban projections derived from 1 km urban surfaces using a dedicated allocation algorithm
- Steps include downscaling from European land-use templates and population projections at the LAD level; decadal updates (2020–2100)
- Protected areas and flood-risk areas excluded as per SSP rules

## Data creation and processing details
- Capitals: description of location resources per 1 km2 cell; natural capitals include land-suitabilities/yields for arable, pastoral, and forest uses
- Agents compete based on the value of service bundles they provide, modulated by behavior and social networks
- Some input data gaps (coast, islands like Shetland) filled with regression or nearest-neighbor approaches
- Normalization applied when 2020 inputs were inconsistent with baselines

## Intensity representation for GIS visualization
- Land-use intensity mapping to aid interpretation: continuous values reflecting management intensity (inputs, technology, production levels)
- Intensity scalars provided per SSP (Table 4) to visualize differences in arable/pasture intensity across decades
- Note: Intensity values are not part of the standard Land Use Indices in the dataset but can be derived for visualization

## Model components and data sources
- Capitals and agent types calibrated from UK-SSP projections and observational data
- Protected areas dataset incorporated; urban areas calibrated with SSP-specific parameters
- Climate (UK-RCPs) and socio-economic (UK-SSPs) inputs drive changes in capital values, agent behavior, service demand, and land-use outcomes
- Model structure and outputs described in Brown et al. (2022) and related Supporting Information

## Model evaluation and limitations
- Evaluation via TRACE (transparent model evaluation) framework; includes unit tests, sensitivity analyses, comparisons with empirical data, and literature
- Online interactive tools available for exploring model outputs
- Limitations:
  - GB-focused only (Northern Ireland data not available consistently)
  - Some coastal/island data gaps addressed with simple methods
  - No direct historical UK land-use reproduction validation due to inconsistent historical datasets
  - Baseline agent typology validated against multiple independent datasets (LCM2015, EUNIS, CEH Land Cover Plus) to support interpretability

## How GIS specialists can use the data
- Use the 1 km stacked rasters to examine land-use trajectories under each UK-RCP-SSP scenario
- Visualize land-use change and compare scenario outcomes across decades
- Utilize the seven-band decadal stacks to create time-series maps or derive transition statistics
- Apply the intensity scalars to map management intensity for arable and pasture classes
- Overlay with protected areas, urban projections, and climate variables for planning and policy analysis
- Integrate with other GIS datasets (coastal, estuarine, and island contexts where data are available) to assess localized impacts

## References and supplementary materials
- Primary dataset and documentation; related methodological papers and supporting information (Calibrations, Tables S1–S8, Figures)
- Key sources include Harmáčková et al. (2022), Merkle et al. (2022), Robinson et al. (2022), Brown et al. (2022) and Brown et al. (2023 dataset citation)