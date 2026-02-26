# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

## Overview
- Maps deposition and concentration to UK protected sites using gridded data and established modelling approaches.
- Combines deposition estimates from CBED with spatial boundaries of SAC, SPA and SSSI, and incorporates NOx and SO2 concentrations from the PCM model.
- Produces multi-resolution datasets (5x5 km grid for site-by-grid, 1x1 km grid for concentrations) and three-year rolling means (2014–2016).

## Data Processing Workflow
- Step 1: Spatial mapping
  - Use Feature Manipulation Engine (FME) to create a UK-wide 5x5 km grid.
  - Clip grid to UK protected site boundaries (SAC/SPA) and derive gridded site datasets.
  - Merge gridded site data with 3-year averaged CBED output (2014–2016) to create a UK protected sites CBED dataset (see Figure 1).
  - Repeat for 1x1 km concentration datasets for NOx and SO2 based on the PCM model.
  - Obtain boundary and feature lists for protected sites from JNCC and national sites (SSSI).
- Step 2: Generating min, max, and grid-average values
  - Compute deposition/concentration statistics per site via SQL on the gridded dataset.
  - Grid-average value calculated as CBEDDepositionValue × (Grid Area / Total Site Area); then sum across grid squares to obtain a site-level grid-average.
  - Outputs include minimum, maximum, and area-weighted (grid-average) values.

## CBED Modelling (Deposition)
- CBED provides 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations, derived from gas/PM concentrations and precipitation-derived wet deposition.
- Dry deposition processes: deposition velocities by land cover (forest, moorland, grassland, arable, urban); applies to appropriate habitats within grid cells; includes gases (SO2, NO2, HNO3, NH3) and particulate matter.
- Wet deposition processes: precipitation deposition plus occult deposition to vegetation; uses an orographic enhancement factor in upland regions.
- Inter-annual variability influenced by weather; results are averaged over three years (rolling mean) to smooth fluctuations.
- Outputs: annual values presented as rolling 3-year means; ecosystem-specific values (moorland, forest) and a grid-average across ecosystems.
- Units: deposition values in keq ha-1 year-1; concentrations in µg m-3.
- Data are derived from the UK Eutrophying and Acidifying Pollutants (UKEAP) network and Defra-led modelling, with extensive QA and peer review.

## PCM Modelling (Concentrations)
- Pollution Climate Mapping (PCM) models generate background maps and 1x1 km grid concentrations for UK pollutants (NOx, NO2, PM, SO2, etc.).
- Runs separate models per pollutant; two components per model: base year and projections.
- Outputs include ~9,000 road-side values; used for scenario assessment, population exposure calculations, and TEN-related applications.
- Used to derive 1x1 km concentration datasets for protected sites.

## Data Structure and Datasets (2014–2016)
- Dataset categories (3-year means, 2014–2016):
  - Datasets 1–3: 5x5 km grid deposition by ecosystem (forest and moorland) per site; include GRIDAREA, YEAR, CENTROID coordinates, and deposition components NH3/NH4, NO2/NO3, and SO2/SO4 for forest or moorland, plus grid-average variants.
  - Dataset 4: 1x1 km ammonia concentration by grid; includes SITEAREA, coordinates, YEAR, and NH3 concentration.
  - Dataset 5: 1x1 km NOx concentration by grid.
  - Dataset 6: 1x1 km SO2 concentration by grid.
  - Dataset 7: Minimum/Maximum/Average deposition to forest across sites (NH3/NH4, NO2/NO3, SO2/SO4) at 5x5 km resolution.
  - Dataset 8: Minimum/Maximum/Average deposition to moorland across sites (NH3/NH4, NO2/NO3, SO2/SO4) at 5x5 km resolution.
  - Dataset 9: (Not fully listed in excerpt; related to forest/moorland deposition values at 5x5 km).
  - Dataset 10: 1x1 km grid-average deposition values (min/max/avg) for NH3/NH4, NO2/NO3, SO2/SO4.
  - Dataset 11: Ammonia concentrations at site level (min/max/avg) for 2014–2016.
  - Dataset 12: Nitrogen oxides concentrations at site level (min/max/avg) for 2014–2016.
- Notes:
  - Data include site codes, site names, grid coordinates, grid areas, designation (SAC/SPA/SSSI), YEAR, and concentration/deposition values.
  - Some fields in the provided excerpts have formatting artifacts; core fields are SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, GRIDAREA, YEAR, and pollutant-specific values.

## Quality Control
- CBED data and calculations have undergone extensive peer review and participated in Defra model inter-comparison exercises.
- Procedures include: documented method development, versioning, central storage of code, and mass-balance checks against previous years.
- Results are widely published in peer-reviewed literature and managed by senior responsible officers.

## Units and Interpretation
- Deposition: keq ha-1 year-1 (can be converted to kg S ha-1 year-1 or kg N ha-1 year-1 using factors 16 and 14, respectively).
  - Total nitrogen deposition = NH3/NH4 + NO2/NO3 components.
- Concentrations: µg m-3 for NH3, NOx, and SO2.
- Notation: Some fields indicate NaN for missing data.

## Access, Sharing, and Governance
- Data are derived from national and UK-wide monitoring networks (e.g., UKEAP) and Defra PCM outputs.
- Data are organized in structured datasets with explicit metadata (site, grid area, year, and pollutant-specific values).
- Documentation and supporting information linked to dataset resources are provided, including model descriptions and references.
- Data are intended to support policy, reporting, and site-specific assessments, with built-in provisions for updates via rolling means.

## Challenges and Considerations for Data Stewards
- Incomplete picture of user needs and priorities for site-specific deposition/concentration data.
- Timely receipt of data from contributors and alignment to standard metadata.
- Ensuring consistent standards across multiple data creators (e.g., forest vs. moorland deposition, grid vs. site-based values).
- Interoperability across multiple formats and resolutions (5x5 km vs 1x1 km grids) and handling large datasets.
- Updating legacy or outdated databases that may require bespoke interoperability solutions.
- Documentation of methodology, versioning, and chain-of-custody to enable reproducibility and long-term stewardship.