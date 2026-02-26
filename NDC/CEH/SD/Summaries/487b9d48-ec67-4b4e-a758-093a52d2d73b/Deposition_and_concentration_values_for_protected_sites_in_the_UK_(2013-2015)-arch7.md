# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Produce gridded maps of deposition and pollutant concentrations for UK protected sites (SAC, SPA, SSSI) using a 3-year rolling mean (2013–2015) to support assessment and policy.

- Overall approach
  - Create a UK-wide 5x5 km grid; clip to protected site boundaries to obtain site-specific gridded data.
  - Merge the gridded site data with 3-year CBED output data to build a UK protected sites CBED dataset.
  - Generate complementary 1x1 km concentration grids for NOx and SO2 from the PCM model.
  - Data sources include boundary/feature lists from JNCC and national sites.

- Step 1: Grid creation and data merging
  - Build 5x5 km grid across Great Britain and clip to SAC/SPA/SSSI boundaries to produce gridded site data.
  - Merge gridded site data with 3-year CBED deposition data (2013–2015) to form UK protected sites CBED dataset.
  - Generate 1x1 km NOx and SO2 concentration datasets from PCM model outputs.
  - Store and reference site attributes (e.g., SITECODE, SITENAME, GRIDAREA, YEAR, DESIGNATION).

- Step 2: Deriving minimum, maximum, and grid-average values
  - For each protected site, compute:
    - Minimum deposition/concentration
    - Maximum deposition/concentration
    - Grid-average deposition/concentration
  - Grid-average calculation (example): CBEDDepositionValue × (GridArea / Total Site area), then sum across overlapping grid cells to yield site-wide grid-average.
  - Data are produced for multiple deposition/concentration components (e.g., NH3/NH4, NO2/NO3, SO2/SO4) and for different ecosystem assumptions.

- Modelling context
  - CBED (Concentration Based Estimated Deposition) modelling produces 5x5 km resolution maps for:
    - Wet and dry deposition of key nitrogen and sulfur species to vegetation
    - Ground-level deposition to different land cover types (forest, moorland, grassland, arable, urban)
    - Seasonal/annual variability is addressed by three-year means; wet deposition accounts for precipitation/occult deposition; dry deposition uses deposition velocities by land cover
  - PCM (Pollution Climate Mapping) modelling provides 1x1 km pollutant concentration maps (NOx, NO2, SO2, PM, etc.) for background and scenario assessments; used for policy support and TEN applications.

- Temporal and ecosystem considerations
  - 3-year rolling means smooth inter-annual deposition variability.
  - Ecosystem-specific values are provided (moorland vs. forest/woodland) and also a grid-average across ecosystems.
  - Values are presented as annual keq per hectare (deposition) and micrograms per cubic meter (concentrations); conversions to kg S/N per ha per year are provided.

- Data outputs and structure (high-level)
  - Datasets cover 2013–2015 averages, at:
    - 5x5 km grid for deposition by site and ecosystem type
    - 1x1 km grid for NOx, NO2, and SO2 concentrations by site
  - Outputs include site-level min, max, and grid-average deposition values, plus concentrations, for each site (SAC/SPA/SSSI).

- Key data fields and formats (examples)
  - Site-level attributes: SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION, YEAR
  - Deposition fields (5x5 km grid): NH3_NH4, NO2_NO3, SO2_SO4_NM (with forest/moorland distinctions), plus grid-average variants
  - Concentration fields (1x1 km grid): NH3_CONC, NO2_CONC, SO2_CONC (and related min/max/avg where provided)
  - Gridarea: area of the grid cell overlapping each site, used in weighting
  - Units: deposition in keq ha-1 year-1; concentrations in µg m-3

- Quality and provenance
  - Methods aligned with QA practices for government analytical models; peer-reviewed and part of model inter-comparison exercises.
  - Documentation, version control, and mass-balance checks are applied.

- References and resources
  - CBED/UK Eutrophying and Acidifying Pollutants modelling literature (e.g., Beswick et al.; Fowler et al.; Dore et al.)
  - PCM model portal and Defra data resources for pollutant deposition and concentration data

- Practical GIS implications
  - GIS workflows rely on clipping grids to protected-site boundaries, aggregating grid values by area weighting, and managing 5x5 km and 1x1 km data layers.
  - Outputs support spatial visualization of deposition/concentration risk across SACs, SPAs, and SSSIs, enabling policy briefings and public-facing maps.