# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Overview
  - Describes how deposition and concentration data are mapped to UK protected sites using CBED and PCM models.
  - Produces 5x5 km grid deposition and 1x1 km grid concentration maps, clipped to SAC, SPA, and SSSI boundaries.
  - Data are rolled 3-year means (2013-2015) and joined with site boundaries to create site-specific CBED datasets.

- Step 1: Spatial mapping workflow
  - Create a UK-wide 5x5 km grid with a data processing tool (FME).
  - Clip the grid to protected site boundaries (.shp) to produce gridded site datasets for SAC/SPA/SSSI.
  - Merge gridded site datasets with 3-year averaged CBED outputs (2013-2015) to form the UK protected sites CBED dataset.
  - Repeat the process for 1x1 km concentration data for NOx and SO2 using the PCM model.
  - Data sources for site boundaries: JNCC and national websites (SSSI).

- Step 2: Generating minimum, maximum, and grid average values
  - Use SQL on the gridded dataset to compute:
    - Minimum, maximum, and grid-average deposition/concentration for each protected site.
    - Grid-average deposition per site is calculated by weighting grid-square deposition by the overlap area with the site (GridArea/TotalSiteArea).
  - Deposition values include CBED deposition mapped to 5x5 km grids and site-area weighting to produce site-level summaries.

- CBED modelling (Concentration Based Estimated Deposition)
  - Generates 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised/reduced nitrogen, and base cations.
  - Based on measured pollutant concentrations in air and ions in precipitation from the UKEAP network.
  - Wet deposition combines precipitation concentrations with an annual UK precipitation map (plus occult deposition to vegetation) and includes an orographic enhancement for uplands.
  - Dry deposition uses concentration maps, deposition velocities by habitat (forest, moorland, grassland, arable, urban), and land-cover weights within each 5x5 km grid.
  - Distinguishes deposition by ecosystem type (moorland vs forest) for critical-load calculations.
  - Averaging across years smooths inter-annual variability; outputs are annual values presented as rolling 3-year means, with ecosystem-specific scenarios (moorland, forest, grid average).

- PCM modelling (Pollution Climate Mapping)
  - Produces background maps and 1x1 km grids of pollutant concentrations for the UK.
  - One model per pollutant (NOx, NO2, PM10, PM2.5, SO2, etc.), with base-year and projection runs.
  - Outputs include background 1x1 km grids and ~9,000 representative roadside values.
  - Used for scenario assessment, population exposure calculations, and TEN applications (PM10, NOx).

- Data sources, quality, and structure
  - Data sources: CBED outputs, PCM outputs, UKEAP measurements, national site boundary data, precipitation data from the UK Met Office.
  - Quality control: peer review, inter-comparison exercises, versioning and documentation, mass-balance checks, and extensive publication of CBED/PCM results.
  - Data structure (examples):
    - Dataset 4: 3-year mean ammonia concentrations for each 5x5 km grid square at each site (SAC/SPA/SSSI).
    - Datasets 1-3: 3-year mean ecosystem-specific deposition (5x5 km) for moorland/forest/ grid average.
    - Dataset 5: 3-year mean NOx concentrations at 1x1 km grid squares.
    - Datasets 7-9: minimum/maximum/average deposition values for moorland/forest at 5x5 km resolution.
    - Dataset 6 and 12: sulfur dioxide and related concentrations at 1x1 km grids.
    - Additional datasets cover grid-average deposition and concentrations for multiple pollutants and ecosystem types.
  - Units and conversion:
    - Deposition values: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 with specified multipliers).
    - Concentrations: µg m-3 for NOx, NO2, NH3, SO2, etc.

- Key considerations for data use
  - Outputs are aligned to UK protected site boundaries and provide both site-specific and grid-averaged views.
  - Three-year rolling means are used to dampen inter-annual variability.
  - Outputs support policy-relevant assessments (e.g., critical load exceedance) and scenario analysis.

- Practical implications for Data Support
  - Requires integrating spatial grid data, site boundary data, and multi-model outputs (CBED and PCM).
  - Involves data cleaning, weighting by site overlap, and aggregation to site-level metrics.
  - Supports development of data products (maps, dashboards, reports) enabling end users to explore deposition/concentration patterns around protected sites.