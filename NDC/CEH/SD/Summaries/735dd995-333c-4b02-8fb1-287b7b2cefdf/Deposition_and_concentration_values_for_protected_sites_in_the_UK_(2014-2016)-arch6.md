# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Create gridded representations of pollutant deposition and concentrations for UK protected sites (SAC, SPA, SSSI) to enable assessment of environmental exposure and potential exceedances.
  - Integrate deposition/concentration data with protected site boundaries to produce site-level metrics.

- Data processing and mapping workflow
  - Use Feature Manipulation Engine (FME) to generate a 5x5 km grid over the UK domain.
  - Clip grid to UK protected site boundaries and merge with 3-year averaged CBED output (2014–2016) to obtain a UK protected sites CBED dataset.
  - Repeat the process for 1x1 km concentration datasets for NOx and SO2 based on PCM model data.
  - Source boundary and site data from JNCC and national websites (SSSI).

- Generating site-level deposition/concentration values
  - Step 2 involves computing minimum, maximum, and grid-average values for each protected site.
  - Grid-average calculation uses: CBEDDepositionValue × (GridArea / Total Site Area), then summing across grids.
  - Resulting values are used to assess potential ecosystem impacts via CBED and PCM.

- CBED modelling (Concentration Based Estimated Deposition)
  - Produces 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised/reduced nitrogen, and base cations.
  - Inputs come from measured air concentrations (gas/PM) and precipitation ion concentrations (from the UKEAP network).
  - Wet deposition: derived from precipitation data plus occult deposition (cloud water deposition) using UK precipitation maps; includes an orographic enhancement factor for upland areas.
  - Dry deposition: uses concentration maps and habitat-specific deposition velocities across five land cover types (forest, moorland, grassland, arable, urban).
  - Decomposition by habitat: moorland applied to non-woodland habitats; forest applied to woodland habitats.
  - Data are annual but provided as rolling 3-year means; three ecosystem-specific outputs are provided (moorland, forest, grid-average) to reflect different vegetation assumptions.
  - Inter-annual variability noted; the 3-year mean smooths variability.

- PCM modelling (Pollution Climate Mapping)
  - Produces background maps and 1x1 km grids of pollutant concentrations for the UK.
  - One model per pollutant (NOx, NO2, PM10, PM2.5, SO2, etc.), each with base year and projection components.
  - Outputs data on a 1x1 km grid plus ~9,000 representative roadside values.
  - Used for scenario assessment, population exposure calculations, and TEN (Time Extension Notification) support.

- Temporal scope and data structure
  - Temporal frame: rolling 3-year means (2014–2016) used for deposition and concentration values.
  - Outputs include:
    - Deposition: 5x5 km grid, ecosystem-specific (moorland/forest) and grid-average 3-year means.
    - Concentrations: 1x1 km grid for NOx and SO2, and ammonia (NH3) concentrations; ecosystem-specific and grid-average options.
  - Units:
    - Deposition: keq ha^-1 year^-1 (reduced nitrogen NH3/NH4 and oxidised nitrogen NO2/NO3, non-marine sulfur SO2/SO4, etc.).
    - Concentrations: µg m^-3 for NH3, NOx, SO2.
  - Data structure highlights (examples):
    - Dataset 4: 3-year mean NH3/NH4 concentrations at site level (NH3_conc in µg/m3).
    - Datasets 1–3: 3-year mean deposition by forest/moorland/grid for 5x5 km grids.
    - Datasets 5–6: 3-year mean NOx/SO2 concentrations at 1x1 km grids.
    - Datasets 7–9: min/max/average deposition to forest/moorland at 5x5 km resolution.
    - Datasets 10–12: min/max/average grid-average concentrations for NH3/NOx/SO2 at 5x5 km or 1x1 km resolutions depending on dataset.

- Data quality and validation
  - QA procedures align with the Government analytical model QA framework.
  - CBED data and calculations have undergone extensive peer review and inter-comparison (Defra model comparison efforts).
  - Method developments are documented, versioned, and stored centrally.
  - Mass-balance checks and comparisons with prior years are routinely performed.

- Data coverage, references, and access
  - Key sources: CBED (Concentration Based Estimated Deposition) data, PCM (Pollution Climate Mapping) model outputs, and UK Eutrophying/Acidifying Pollutants networks (UKEAP).
  - Supporting references include peer-reviewed studies and RotAP reviews; multiple citations listed for model development and validation.
  - Access and background information:
    - UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information
    - UK Air Defra PCM data and network information pages
  - Data are designed to support regulatory reporting, exposure assessment, and policy analysis.

- Practical considerations for data support
  - Handling patchy or heterogeneous data requires mapping data to protected-site boundaries and choosing appropriate ecosystem assumptions (moorland vs. forest vs. grid-average).
  - Outputs are prepared as rolling 3-year means to mitigate inter-annual variability; users should be aware of temporal smoothing when interpreting recent-year signals.
  - Several datasets provide minimum/maximum/average values to capture within-site variability and range of possible deposition/concentration scenarios.

- Notes on data interpretation
  - Wet deposition incorporates precipitation patterns and orographic effects; dry deposition depends on land cover and deposition velocities.
  - Conversion factors are provided to translate keq ha^-1 year^-1 to kg ha^-1 year^-1 for S and N.
  - Coverage includes multiple UK protected site types and grid-based aggregations to support self-serve data exploration and reporting.