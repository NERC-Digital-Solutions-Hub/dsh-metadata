# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose
  - Map deposition and concentration of pollutants to UK protected sites (SAC, SPA, SSSI) using 5x5 km and 1x1 km grids.
  - Integrate CBED (Concentration Based Estimated Deposition) outputs with protected-site boundaries and generate site-level deposition/concentration values.
  - Produce three-year rolling means (2015–2017) and ecosystem-specific as well as grid-average values.

- Processing workflow (beginning to end)
  - Step 1: Create a 5x5 km UK grid, clip to protected-site boundaries, and generate a gridded dataset for SAC/SPA/SSSI. Merge with 3-year averaged CBED data via FME to produce UK protected-site CBED dataset.
  - Step 2: Compute minimum, maximum, and grid-average deposition/concentration for each site using SQL on the gridded data. Calculate grid-area-weighted averages to aggregate to site level.
  - Data inputs include boundary/feature lists for protected sites downloaded from national sources; CBED modelling outputs; PCM model outputs for background concentrations.

- Modelling frameworks
  - CBED (Concentration Based Estimated Deposition)
    - Produces 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised/reduced nitrogen, and base cations from gas/PM and precipitation data (UKEAP network).
    - Wet deposition combines gas/particle concentrations with precipitation, including occult deposition; uses an orographic enhancement factor for uplands.
    - Dry deposition uses deposition velocities by land cover (forest, moorland, grassland, arable, urban) and is combined per grid cell with land-cover composition.
    - Time handling: annual values but presented as rolling 3-year means; inter-annual variability acknowledged.
    - Ecosystem-specific outputs include moorland, forest, and a grid-average scenario.
  - PCM (Pollution Climate Mapping)
    - Produces background pollutant concentration maps on a 1x1 km grid and ~9,000 representative roadside values.
    - Used for scenario assessment, population exposure calculations, and support for policy development and TEN applications.
    - Each pollutant model has base-year and projection components.

- Data structure and formats (highlights)
  - Data produced as 3-year means (2015–2017) with multiple datasets and grid resolutions:
    - Datasets at 5x5 km: ecosystem-specific deposition (NH3/NH4, NO2/NO3, SO2/SO4 NM) by grid; grid-average deposition; site-level summaries.
    - Datasets at 1x1 km: concentrations of NOx, NO2, SO2, NH3, and related components by grid.
    - Site-level summaries include minimum, maximum, and averaged values for each deposition/concentration component, by ecosystem type and grid average.
  - Specific dataset naming conventions indicate site code, site name, area, grid centroid coordinates, country, designation (SAC/SPA/SSSI), grid area, year, and pollutant-specific values (e.g., NH3_NH4_FOREST, NO2_NO3_MOORLAND, SO2_SO4_NM_FOREST, NO2_CONC, NH3_CONC, SO2_CONC, etc.).

- Units and data interpretation
  - Deposition: all deposition values are in keq ha^-1 year^-1; can be converted to kg S ha^-1 year^-1 (multiply by 16) or kg N ha^-1 year^-1 (multiply by 14).
  - Concentrations: all concentration values are in µg m^-3.
  - Total nitrogen deposition is the sum of NO2_NO3 and NH3_NH4 components.

- Quality control and reproducibility
  - Methods align with government QA practices for analytical models; extensive peer review of CBED data and methods; participation in model inter-comparison exercises.
  - Documentation, versioning, and central storage of code; mass-balance checks to ensure numerical consistency; comparison to previous years.

- Data access and documentation
  - Data sources and model information referenced via Defra/CEH and UK-AIR resources.
  - Detailed dataset descriptors include SITECODE, SITENAME, SITEAREA, CENTROID coordinates, GRIDAREA, YEAR, designation, and pollutant-specific values (with clear unit definitions).

- Typical challenges addressed (data steward perspective)
  - Handling large, multi-system datasets and multiple grid resolutions (5x5 km vs 1x1 km).
  - Aligning protected-site boundaries with gridded CBED/PCM outputs.
  - Ensuring timely data provision and consistent metadata for site-level aggregation.
  - Managing ecosystem-specific vs grid-average summaries and maintaining transparent documentation of methods.

- References and resources
  - CBED/UK Eutrophying and Acidifying Pollutants materials; PCM data and model descriptions; supporting information and methodological references.
  - Resource locators include UK pollutant deposition and PCM data portals, Defra/UK-AIR pages, and related scientific publications.

- Endnotes on data specifics (summary of data structure)
  - Dataset 4: NH3/NH4 concentration (3-year mean, 5x5 km grid; site-level associations).
  - Datasets 1–3: 3-year mean, 5x5 km grid for forest/moorland deposition and corresponding grid-average values.
  - Dataset 5: NOx concentrations (1x1 km grid).
  - Dataset 6: SO2 concentrations (1x1 km grid).
  - Datasets 7–9: site-level min/max/avg deposition by ecosystem (moorland/forest) at 5x5 km resolution.
  - Dataset 10: grid-average deposition values by site (min/max/avg) across NO2/NH3/SO2 components.
  - Datasets 11–12: site- and grid- average concentrations for NH3 and NO2/NOx/SO2, respectively.

- Practical implications for data stewardship
  - Provides a comprehensive, standardized framework for integrating emissions/atmospheric chemistry models with protected-site geographies.
  - Emphasizes robust metadata, version control, and reproducible workflows for governance and data sharing.
  - Supports policy-relevant assessments (e.g., critical load exceedances) with clearly defined units, aggregations, and temporal harmonization.