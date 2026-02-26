# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose and scope
  - Documents how CBED (Concentration Based Estimated Deposition) and PCM (Pollution Climate Mapping) data are produced and organized for UK protected sites (SAC, SPA, SSSI).
  - Provides 3-year rolling mean outputs (2017–2019) and grid-based deposition and concentration values to support assessment of ecosystem exposure and potential exceedances of critical loads.
  - Outputs are aligned to protected-site boundaries using 5x5 km grids (and 1x1 km grids for concentrations), with site-level aggregation and ecosystem-specific deposition patterns (moorland, forest) or grid-average values.

- Modelling approaches

  - CBED modelling
    - Generates 5x5 km resolution maps of wet and dry deposition for nitrogen and sulfur compounds and base cations from measured air concentrations and precipitation data (UKEAP network).
    - Dry deposition: combines gas/PM concentrations with habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
    - Wet deposition: includes precipitation deposition plus occult deposition to vegetation; uses precipitation maps and sea-salt separation for sulfur and calcium.
    - Orographic enhancement factor accounts for increased precipitation and deposition in upland areas.
    - Annual values are averaged into a 3-year mean to smooth inter-annual variability; outputs include forest/moorland/grid-average deployments.
    - Data are provided as 3-year means across three ecosystem assumptions: moorland everywhere, forest everywhere, and a grid-average; non-marine Ca+Mg values are only for 2019.

  - PCM modelling
    - Produces background concentration maps on a 1x1 km grid for the UK, with separate models per pollutant (NOx, NO2, PM10, PM2.5, SO2, etc.).
    - Provided in base-year and projection formats; used for scenario assessment, population exposure calculations, and regulatory reporting (TEN applications for PM10/NOx).
    - Outputs include around 9,000 representative road-side values and support policy development.

- Key data outputs and data structure

  - Site-specific grid mapping and aggregation
    - Step 1: Spatially map deposition and concentration to UK protected sites by clipping 5x5 km grids to SAC/SPA/SSSI boundaries.
    - Step 2: Compute minimum, maximum, and grid-average values for each site using area-weighted sums within grid squares.
    - Outputs are organized into a set of CSV files (12 main data files) describing deposition and concentration by site, grid, and ecosystem type, for 2017–2019.

  - File overview (examples)
    - File 1 APIS_deposition_forest_sitebygrid_2017_2019.csv: 3-year mean deposition to forest by 5x5 km grid, with keq ha-1 year-1 units.
    - File 2 APIS_deposition_moorland_sitebygrid_2017_2019.csv: deposition to moorland by grid.
    - File 3 APIS_deposition_gridaverage_sitebygrid_2017_2019.csv: grid-average deposition by site.
    - File 4 APIS_ammonia_concentration_sitebygrid_2017_2019.csv: ammonia concentration by grid (µg m-3).
    - File 5 APIS_nox_concentration_sitebygrid_2017_2019.csv: NOx concentration by grid (µg m-3).
    - File 6 APIS_so2_concentration_sitebygrid_2017_2019.csv: SO2 concentration by grid (µg m-3).
    - File 7 APIS_deposition_forest_site_2017_2019.csv: min, max, and average deposition to forest for NOx, NHx, SOx, and Ca+Mg.
    - File 8 APIS_deposition_moorland_site_2017_2019.csv: min, max, and average deposition to moorland.
    - File 9 APIS_deposition_gridaverage_site_2017_2019.csv: min, max, and average deposition grid-average values.
    - File 10 APIS_ammonia_concentration_site_2017_2019.csv: max/min/avg ammonia concentrations across sites.
    - File 11 APIS_nox_concentration_site_2017_2019.csv: max/min/avg NOx concentrations across sites.
    - File 12 APIS_so2_concentration_site_2017_2019.csv: max/min/avg SO2 concentrations across sites.
    - Each file includes site identifiers, site area, grid coordinates, year, and relevant concentration or deposition metrics.

- Units and interpretation

  - Deposition values: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 using standard multipliers: S = keq × 16; N = keq × 14; total N = NO2_NO3 + NH3_NH4).
  - Concentration values: µg m-3 (for NH3, NOx, SO2).
  - 3-year means: reported as rolling means to smooth interannual variability inherent in weather and emissions.

- Quality control and governance

  - Methods aligned with QA practices for government models; subject to extensive peer review and participation in Defra model inter-comparison exercises.
  - Version control, documentation of method developments, and central storage of code.
  - Mass-balance checks and consistency reviews against prior years; results widely published in peer-reviewed literature.

- Relevance for monitoring, evaluation, and policy

  - Provides standardized, site-relevant deposition and concentration metrics to evaluate environmental health and potential exceedances of critical loads for protected ecosystems.
  - Supports policy development, scenario analysis, and official reporting requirements (e.g., TEN applications for PM10/NOx).
  - Data governance considerations highlighted, including data sharing and the need to ensure traceability of inputs and methodologies.

- Notable methodological details and caveats

  - CBED dependencies: concentration maps, precipitation data, habitat-specific deposition velocities, and orographic adjustments; interannual variability driven by weather patterns.
  - Wet vs. dry deposition separation and sea-salt corrections for sulfur and calcium.
  - For non-marine Ca+Mg values, different ecosystem assignments and independent treatment across forest/moorland outputs.
  - Data are provided for a three-year rolling period (2017–2019) with some components (e.g., non-marine Ca+Mg) calculated for 2019 only.