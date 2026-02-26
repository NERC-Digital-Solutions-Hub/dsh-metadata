# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- A methodological description of mapping, modelling, and reporting deposition and concentration of air pollutants across UK protected sites (SAC, SPA, SSSI) to inform environmental policy and monitoring frameworks.
- Focus on generating gridded, site-specific deposition and concentration metrics to assess ecological exposure and potential exceedances.

## Objectives and scope for monitoring frameworks
- Identify and produce environmental health measures (deposition and concentration) to scrutinise policy and inform future decision-making.
- Provide site- and grid-scale indicators (min, max, and area-weighted averages) across protected sites for nitrogen, sulfur, base cations, and related pollutants.
- Support assessment of ecosystem impacts and potential exceedances of critical loads.

## Data sources and modelling approaches
- CBED (Concentration Based Estimated Deposition) modelling:
  - Produces 1x1 km resolution maps of wet and dry deposition for S, N, and base cations using concentration and precipitation data from the UK Eutrophying and Acidifying Pollutants network (UKEAP) and UK Met Office precipitation data.
  - Dry deposition uses habitat-specific deposition velocities for five land-cover categories (forest, moorland, grassland, arable, urban).
  - Wet deposition includes direct deposition, occult deposition, and separation of anthropogenic vs total components; includes orographic enhancement for uplands.
  - Outputs are annual values aggregated to 3-year means (2018–2020), with ecosystem-specific scenarios (moorland, forest/woodland, grid average).
- PCM (Pollution Climate Mapping) modelling:
  - Produces background concentration maps on a 1x1 km grid for UK pollutants (NOx, NO2, PM10/2.5, SO2, etc.), including road-side values.
  - Used for scenario assessment, population exposure, and TEN reporting obligations.

## Step-by-step methodological workflow
- Step 1: Spatial mapping to UK protected sites
  - Create a 1x1 km grid for the UK; clip to SAC/SPA/SSSI boundaries.
  - Merge gridded CBED deposition data with site boundaries to create a UK protected sites CBED dataset.
  - Repeat for 1x1 km concentration datasets (NOx, SO2) using PCM outputs.
- Step 2: Generate minimum, maximum, and grid-average values
  - Use SQL on the gridded dataset to compute grid-average deposition/concentration for each site.
  - Grid-average value calculated as: CBED deposition value × (Grid Area / Total Site Area), then summed across overlapping grids (area-weighted).
  - Outputs include site-level minimum, maximum, and area-weighted averages; and grid-average values across 5 land-cover categories.

## CBED and PCM modelling details
- CBED outputs:
  - Wet deposition (SO4, NH4, NO3, Ca, Mg, acidity) and dry deposition (gas and PM to vegetation) across 5 land-cover types.
  - Annual values, provided as rolling 3-year means; ecosystem-specific values for moorland/short vegetation, forest, or grid average.
- PCM outputs:
  - Background pollutant concentrations on 1x1 km grids, plus road-side values; used for scenario analyses and exposure calculations.
- Timeframe and averaging:
  - 3-year rolling means used to smooth inter-annual variability; non-marine Ca+Mg values treated separately.

## Outputs and data structure
- A suite of files (2018–2020 rolling means) detailing:
  - Deposition by forest and moorland ecosystems (NH3/NH4, NO2/NO3, SO2/SO4, Ca/Mg), and grid-average values.
  - Concentrations of ammonia (NH3), nitrogen oxides (NOx/NO2), and sulfur dioxide (SO2) for grid squares and site-based aggregations.
  - Minimum, maximum, and average values for each pollutant and component, across forest/moorland and grid-average contexts.
- Output resolutions: 1x1 km grids; site-level summaries with site-area overlaps and grid-area weighting.

## Units and data interpretation
- Deposition: keq ha-1 year-1 (converted to kg S ha-1 year-1 or kg N ha-1 year-1 as needed using multipliers).
- Concentrations: µg m-3 (µg/m3) for NH3, NOx, and SO2.
- Key conversions:
  - Sulphur deposition: keq ha-1 year-1 × 16 = kg S ha-1 year-1.
  - Nitrogen deposition: keq ha-1 year-1 × 14 = kg N ha-1 year-1.
  - Total nitrogen deposition = NO2/NO3 + NH3/NH4.
- Presentation of outputs:
  - Three-year means for most values; detailed files provide min/max/average for forest, moorland, and grid-average categories.

## Quality control and governance
- Methods align with the Review of quality assurance of Government analytical models.
- CBED and PCM results validated via peer-reviewed literature and Defra model inter-comparison exercises.
- Mass-balance checks and version control procedures; data documentation and central storage of code.

## Data structure and file highlights
- File inventories include:
  - Site-by-grid deposition data for forest (File 1), moorland (File 2), and grid-average (File 3).
  - Ammonia concentration (Files 4, 9, 10) and NOx (Files 5, 11) and SO2 (Files 6, 12) concentration datasets.
  - Deposition datasets with minimum/maximum/average values by ecosystem (Files 7, 8) and grid-average counterparts (File 9, 10).
  - Metadata fields cover SITECODE, SITENAME, SITEAREA, geographic coordinates, designated site type, and YEAR.

## Relevance for monitoring frameworks and policy evaluation
- Provides standardized, transparent measures of atmospheric deposition and concentration relevant to environmental health, ecosystem exposure, and policy evaluation.
- Supports assessment of potential exceedances against ecological thresholds such as critical loads and informs exposure-based decision-making and scenario planning.
- Highlights data governance considerations for openness, metadata completeness, timeliness, and interoperability across organisations.

## References and resources
- UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information (URL and references provided in the document).
- PCM model resources and Defra-related data portals (linked in the resource section).
- Key methodological references for CBED/PCM; inter-comparison and validation studies cited (e.g., Carslaw 2011; Fowler et al. 1988; Dore et al. 2001, 2007).