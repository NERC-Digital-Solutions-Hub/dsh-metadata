# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose and scope
  - Describes methods to map and evaluate deposition and concentration of key atmospheric pollutants across the UK, focusing on protected sites (SAC, SPA, SSSI) and informing policy decisions.
  - Uses two modelling streams: CBED (Concentration Based Estimated Deposition) for deposition and PCM (Pollution Climate Mapping) for background concentrations.
  - Outputs are aggregated to 5x5 km grid squares and 1x1 km concentration grids, with 3-year rolling means (2015–2017) to smooth inter-annual variability.

- CBED modelling overview
  - Deposition targets: wet and dry deposition of sulphur, oxidised and reduced nitrogen, and base cations to vegetation.
  - Data foundations: site-based measurements interpolated to UK-wide concentration maps; ions in precipitation combined with national precipitation maps to yield wet deposition; gas/PM concentrations combined with habitat-specific deposition velocities to produce dry deposition for five land-cover categories (forest, moorland, grassland, arable, urban).
  - Wet deposition components: includes occult (cloud droplet) deposition; separates anthropogenic vs total sulphur and calcium using sea-water ion ratios; includes orographic enhancement for uplands.
  - Temporal aspect: deposition values are averaged over a rolling 3-year period (2015–2017) to reduce inter-annual fluctuations.
  - Ecosystem assumptions: outputs provided for three ecosystem scenarios at each grid cell—moorland/short vegetation everywhere, forest everywhere, and a grid-average across ecosystems.

- PCM modelling overview
  - Purpose: produce background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) to support policy development, exposure assessment, and regulatory reporting.
  - Outputs: per-pollutant models with base-year and projection runs; roughly 9,000 representative roadside values; used for scenario assessment and TEN (Time Extension Notification) support.

- Spatial processing steps
  - Step 1: Spatial mapping to protected sites
    - Create a UK-wide 5x5 km grid; clip to SAC/SPA/SSSI boundaries; merge with 3-year CBED deposition data to produce site-level grids (CBED deposition bounded by site areas).
    - Extend to 1x1 km NOx and SO2 concentration grids derived from PCM.
    - Data sources: protected-site boundaries and site metadata from national sources.
  - Step 2: Deriving minimum, maximum, and grid-average deposition/concentration per site
    - Use SQL to compute per-site min, max, and grid-average values from the gridded data.
    - Grid-average calculation: grid-square area weighed by site area via CBED deposition values: CBEDDepositionValue × (GridArea / TotalSiteArea), then summed to yield a site-level value.

- Data structure and content
  - CBED deposition and PCM concentration data are organized into multiple datasets, covering:
    - 5x5 km grid deposition by land-cover (moorland, forest) and grid-average (Datasets 1–3).
    - 1x1 km concentration grids for NOx, SO2 (Datasets 5–6).
    - 3-year mean concentrations for ammonia (NH3) and nitrogen oxides broken down by forest/moorland/grid-average (Datasets 4, 11–12).
    - Minimum, maximum, and average deposition/concentration values for site-level summaries (Datasets 7–9, 10).
  - Units and conversions
    - Deposition values are expressed as keq ha-1 year-1; conversion to kg per ha per year is:
      - Sulphur deposition: keq ha-1 year-1 × 16 = kg S ha-1 year-1
      - Nitrogen deposition: keq ha-1 year-1 × 14 = kg N ha-1 year-1
    - Concentration values are expressed as µg m-3.
  - Specific dataset examples (descriptions)
    - Dataset 1: APIS_n_acid_dep_forest_bygrid_2015_2017.csv — forest deposition by 5x5 km grid.
    - Dataset 2: APIS_n_acid_dep_moorland_bygrid_2015_2017.csv — moorland deposition by 5x5 km grid.
    - Dataset 3: APIS_n_acid_dep_gridavg_bygrid_2015_2017.csv — grid-average deposition by 5x5 km grid.
    - Dataset 4: APIS_nh3_conc_bygrid_2015_2017.csv — ammonia concentration by 5x5 km grid.
    - Dataset 5: APIS_nox_conc_bygrid_2015_2017.csv — NOx concentration by 1x1 km grid.
    - Dataset 6: APIS_so2_conc_bygrid_2015_2017.csv — SO2 concentration by 1x1 km grid.
    - Dataset 7–9: Generated site-level min/max/average deposition to forest/moorland across sites (forest and moorland).
    - Dataset 10: APIS_n_acid_dep_gridavg_site_2015_2017.csv — grid-average deposition at site level.
    - Dataset 11: APIS_nh3_conc_site_2015_2017.csv — NH3 concentration at site level.
    - Dataset 12: APIS_nox_conc_site_2015_2017.csv — NOx concentration at site level.
    - APIS_so2_conc_site_2015_2017.csv — SO2 concentration at site level (structure described with columns for site metadata and concentrations).

- Data quality and governance
  - Methods aligned with QA practices for government analytical models.
  - CBED data and calculations have undergone extensive peer review and inter-comparison exercises; mass-balance checks are routinely performed.
  - Version control and central storage of model code; results widely published in peer-reviewed literature.
  - Documentation provides detailed data structure, metadata, and field definitions to support traceability and re-use.

- Accessibility and references
  - Data and model information available via CEH/Defra portals:
    - UK Acidifying and Eutrophying Atmospheric Pollutants portal
    - UK Air Defra networks information (ukeap)
    - PCM data repository
  - Supporting references and background materials included for methodological validation and historical context.