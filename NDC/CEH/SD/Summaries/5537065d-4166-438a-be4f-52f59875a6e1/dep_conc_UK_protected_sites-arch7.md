# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Create map-based data products showing deposition and concentration on UK protected sites (SAC, SPA, SSSI) to enable spatial understanding and analysis.
  - Integrate CBED (3-year mean 2015–2017) and PCM NOx/SO2 concentration data with protected-site boundaries for GIS use.

- Step 1: Grid creation and data fusion
  - Generate a 5x5 km grid covering the UK domain.
  - Clip grids to UK protected site boundaries (SAC, SPA, SSSI) to produce site-specific gridded data.
  - Merge these gridded data with the 3-year averaged CBED output (2015–2017) to form the UK protected sites CBED dataset (reference Figure 1).
  - Repeat for 1x1 km concentration datasets for NOx and SO2 using the PCM model.
  - Source boundary and feature lists for protected sites are downloaded from national websites.

- Step 2: Derivation of min, max, and grid-average values
  - For each protected site, compute:
    - Minimum deposition/concentration
    - Maximum deposition/concentration
    - Grid-average deposition/concentration
  - Method: SQL on the Step 1 gridded dataset; grid-average is computed by weighting grid-square area by site area and applying the CBED value:
    - CBEDDepositionValue × (Grid Area / Total Site Area)
  - Aggregation across grid squares yields the site-level grid-average value.

- CBED modelling (background)
  - Purpose: Generate 5x5 km resolution maps of wet and dry deposition for nitrogen, sulphur, and base cations from gas/particle concentrations (air) and precipitation chemistry (ions in precipitation).
  - Data sources and processes:
    - Concentrations interpolated from UK EMEP/UKEAP network measurements.
    - Wet deposition derived from precipitation plus occult deposition (cloud interception) using annual precipitation maps.
    - Dry deposition computed for five land-cover categories (forest, moorland, grassland, arable, urban) using habitat-specific deposition velocities.
    - Dry deposition accounts for deposited gases (SO2, NO2, HNO3, NH3) and particulates (sulfate, nitrate, ammonium, calcium, magnesium).
    - Moorland vs forest routing: forest values for woodland, moorland values for non-woodland habitats.
    - Annual variability is addressed by using a rolling 3-year mean (to smooth inter-annual variation).
  - Outputs and time frame:
    - Annual values aggregated to rolling 3-year means, ecosystem-specific (moorland/short vegetation vs forest) and grid-average.
  - Quality and references:
    - Peer reviewed and used in Defra model inter-comparison exercises.
    - Mass balance checks and version control procedures.

- PCM modelling (background)
  - Purpose: Produce background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) across the UK.
  - Details:
    - A suite of models per pollutant (base year and projection models) run by Ricardo Energy & Environment for Defra.
    - Outputs include 1x1 km grid data plus ~9,000 roadside values.
    - Used for scenario assessment, population exposure calculations, and regulatory reporting (TEN applications for PM10/NOx).

- Data products and datasets (structure and content)
  - Data structure describes 12 datasets (2015–2017 rolling three-year means) with 5x5 km and 1x1 km resolutions, plus site-level summaries.
  - Dataset overview (selected highlights):
    - Dataset 1: APIS_n_acid_dep_forest_bygrid_2015_2017.csv – 5x5 km grid, forest-deposition components (NH3/NH4, NO2/NO3, SO2/SO4 NM) by site; includes SITECODE, SITENAME, SITEAREA, GRIDAREA, YEAR.
    - Dataset 2: APIS_n_acid_dep_moorland_bygrid_2015_2017.csv – 5x5 km grid, moorland deposition components; similar structure to Dataset 1.
    - Dataset 3: APIS_n_acid_dep_gridavg_bygrid_2015_2017.csv – 5x5 km grid-average deposition components by grid; per-site context.
    - Dataset 4: APIS_nh3_conc_bygrid_2015_2017.csv – 5x5 km grid ammonia concentrations (NH3) by site.
    - Dataset 5: APIS_nox_conc_bygrid_2015_2017.csv – 1x1 km grid NOx concentrations by site.
    - Dataset 6: APIS_so2_conc_bygrid_2015_2017.csv – 1x1 km grid SO2 concentrations by site.
    - Dataset 7: APIS_n_acid_dep_forest_site_2015_2017.csv – per-site minimum/maximum/average forest deposition (NO2/NO3, NH3/NH4, SO2/SO4) across sites.
    - Dataset 8: APIS_n_acid_dep_moorland_site_2015_2017.csv – per-site minimum/maximum/average moorland deposition components.
    - Dataset 9: APIS_n_acid_dep_gridavg_site_2015_2017.csv – per-site minimum/maximum/average grid-average deposition across forest/moorland/grid contexts.
    - Dataset 10: APIS_n_acid_dep_gridavg_site_2015_2017.csv – (alternative naming in the source) grid-average deposition metrics by site with min/max/avg across grid categories.
    - Dataset 11: APIS_nh3_conc_site_2015_2017.csv – site-level NH3 concentrations (max/min/avg).
    - Dataset 12: APIS_nox_conc_site_2015_2017.csv – site-level NOx concentrations (max/min/avg).
    - APIS_so2_conc_site_2015_2017.csv – site-level SO2 concentrations (max/min/avg).
  - Units and interpretation
    - Deposition values: keq ha-1 year-1 (convertible to kg S ha-1 or kg N ha-1 via factors: S ×16, N ×14).
    - Concentrations: µg m-3 (µg m-3 for NH3, NOx, SO2).
  - Coverage and resolutions
    - 5x5 km grids for deposition by ecosystem and grid-average values.
    - 1x1 km grids for concentration fields (NOx, SO2).
    - Site-level data provide min/max/average values for each site.

- Data quality and validation
  - QA/alignment with Government QA frameworks.
  - Peer review of CBED data and calculations; involvement in inter-comparison exercises.
  - Documentation, version control, and mass-balance checks to ensure numerical consistency.

- Access and references
  - Core data sources and supporting information:
    - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) and CBED/PCM data portals.
    - PCM data and model pages for NOx, NO2, SO2, etc.
  - Selected references for methodological background and validation (e.g., Holme Moss studies, inter-comparison reports).

- Practical GIS implications for users
  - Enables overlay of protected-site polygons with 5x5 km and 1x1 km deposition/concentration surfaces.
  - Supports extraction of site-specific exposure and deposition metrics (min/max/average) under different ecosystem assumptions.
  - Provides structured, time-consistent 3-year means (2015–2017) suitable for trend analysis and policy impact assessments.