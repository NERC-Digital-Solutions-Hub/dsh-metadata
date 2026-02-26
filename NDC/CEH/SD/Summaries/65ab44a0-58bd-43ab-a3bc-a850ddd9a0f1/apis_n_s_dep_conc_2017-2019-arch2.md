# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose: document the data and modelling methods used to map deposition and concentrations of acidifying and eutrophying pollutants to UK protected sites (SAC, SPA, SSSI), enabling environmental health assessment and policy monitoring over time.

- Key datasets and sources:
  - CBED (Concentration Based Estimated Deposition) data for 2017–2019 (3-year means): 5x5 km grid, supports deposition to protected sites, including wet and dry deposition components.
  - PCM (Pollution Climate Mapping) model outputs for 1x1 km grids: background pollutant concentrations (NOx, NO2, SO2, PM, etc.) plus representative road-side values, used for scenario evaluation and exposure assessments.
  - UK protected site boundaries and area data (SAC, SPA, SSSI/ASSI) clipped to the 5x5 km grid.
  - Ecosystem-specific deposition categories (moorland, forest/woodland) and non-marine Ca+Mg deposition.

- Step 1: Spatial mapping workflow
  - Create a UK-wide 5x5 km grid and clip to protected site boundaries (SAC/SPA/SSSI).
  - Merge gridded CBED outputs (3-year mean 2017–2019) with site boundaries to produce a UK protected sites CBED dataset (illustrated in Figure 1).
  - For NOx and SO2, use 1x1 km PCM concentration datasets and integrate as part of the site-level data.

- Step 2: Deriving deposition/concentration values for each site
  - Compute minimum, maximum, and grid-average deposition/concentration for each protected site using SQL on the gridded data.
  - Grid-average calculation: CBED deposition value × (GridArea / TotalSiteArea), then sum across grid squares within the site.
  - Outputs cover multiple deposition components and ecosystem scenarios (e.g., moorland vs forest).

- CBED modelling details
  - Purpose: estimate deposition of nitrogen and sulfur species and base cations to vegetation across land covers.
  - Components:
    - Wet deposition (precipitation-based, including occult deposition to vegetation).
    - Dry deposition (gas and particulate matter to vegetation), using habitat-specific deposition velocities for five land-cover categories: forest, moorland, grassland, arable, urban.
    - Separation of anthropogenic vs total components for certain species using sea-salt corrections.
    - Orographic enhancement accounts for upland precipitation effects (Great Dun Fell, Holme Moss studies cited).
  - Variability and temporal aspects:
    - Inter-annual variability influenced by weather; three-year rolling means used to smooth fluctuations.
    - Outputs provided as annual values but presented as rolling 3-year means, except non-marine Ca+Mg values (2019 only).
  - Outputs and units:
    - Depositions: keq ha-1 yr-1 (convertible to kg S or N ha-1 yr-1).
    - Concentrations: µg m-3 (NH3, NOx, SO2).

- PCM modelling details
  - Purpose: produce background concentration maps on a 1x1 km grid for various pollutants (NOx, NO2, PM10, PM2.5, SO2, etc.), aligning with EU reporting requirements.
  - Features:
    - Separate base-year and projection models; runs for policy support, TEN applications, and exposure calculations.
    - About 9,000 representative roadside values incorporated.
  - Outputs and units: concentration values in µg m-3.

- Data structure and accessibility
  - A suite of data files (12+ in total) provides:
    - Site-by-grid and grid-average deposition values (5x5 km) by ecosystem type (forest and moorland) and overall grid averages.
    - 3-year mean concentrations for ammonia, NOx, NO2, and SO2 at 5x5 km or 1x1 km resolutions as appropriate.
    - Minimum, maximum, and average deposition values for forest and moorland across sites.
    - Metadata for sites: SITECODE, SITENAME, SITEAREA, centroids, GRIDAREA, COUNTRY, DESIGNATION, YEAR, etc.
  - Units and data notes:
    - Depositions in keq ha-1 yr-1; concentrations in µg m-3.
    - Non-marine Ca+Mg deposition values sometimes provided separately; certain files include year-specific or ecosystem-specific aggregations.

- Quality control and rigor
  - Extensive peer review and inter-comparison (e.g., Defra context and related papers).
  - Version control, method documentation, and central code management.
  - Mass-balance checks to ensure numerical consistency with previous years.

- Practical use for Analysts Monitoring the Environment
  - Provides standardized, trackable datasets to assess environmental health against standards over time.
  - Enables spatial visualization via grids and site-level summaries (maps, charts, reports).
  - Supports policy performance analysis through 3-year rolling means and ecosystem-specific deposition scenarios.
  - Emphasizes data transparency and reuse by storing datasets and enabling access to underlying input data.

- Challenges and opportunities highlighted for analysts
  - Increasing the value of monitoring datasets by integrating CBED/PCM outputs with other environmental data (e.g., habitat changes, biodiversity metrics).
  - Making underlying data accessible to users beyond final outputs to facilitate broader reuse and validation.