# Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Objective
  - Build map-based data products to understand deposition and concentration impacts on UK protected sites by integrating CBED/PCM outputs with site boundaries.

- GIS workflow and data integration
  - Create a 5x5 km UK-wide grid, clip to UK protected sites (SAC, SPA, SSSI) to produce site-specific gridded data.
  - Merge gridded CBED 3-year mean data (2016–2018) with the clipped grid data using FME.
  - Repeat the process for 1x1 km NOx and SO2 concentration datasets from PCM.
  - Source boundary and site feature data from each country’s national websites.

- Step 1 output
  - UK protected sites CBED dataset: gridded deposition/concentration data aligned to site boundaries.

- Step 2: Deriving minimum, maximum, and grid-average values
  - For each protected site, compute min, max, and grid-average deposition/concentration via SQL on the gridded dataset.
  - Grid-average calculation: grid value × (Grid Area / Total Site Area), then sum across grids within the site.
  - Formula reference: CBEDDepositionValue × (GridArea / TotalSiteArea).

- CBED modelling overview (deposition)
  - Generates 5x5 km resolution maps of wet and dry deposition for S, N, and base cations using air concentration measurements and precipitation data from the UKEAP network.
  - Wet deposition combines gas/particle chemistry with annual precipitation; includes occult deposition and orographic enhancement.
  - Dry deposition uses concentration maps, habitat-specific deposition velocities, and 5 land-cover categories (forest, moorland, grassland, arable, urban).
  - Deposition to forest vs. moorland habitats reflects ecosystem-specific assumptions; inter-annual variation smoothed by 3-year means.
  - Outputs provided as annual values but presented as rolling 3-year means (three ecosystem-specific scenarios: moorland, forest, grid average).

- PCM modelling overview (concentration)
  - Produces background maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) for the UK.
  - Used for scenario assessment, exposure calculations, and policy support; runs include base-year and projections; includes ~9,000 roadside values.

- Data integrity and quality control
  - Methods QA aligned with government model QA guidance; extensive peer review and inter-comparison involvement (e.g., Carslaw 2011).
  - Version control, method documentation, central code repository, and mass-balance checks routinely performed.

- Dataset structure and content (3-year means, 2016–2018)
  - Datasets combine grid- and ecosystem-specific deposition (5x5 km) and concentrations (1x1 km) for SAC/SPA/SSSI.
  - Examples of datasets:
    - Dataset 4: NH3/NH4 concentration (grid-level 5x5 km)
    - Dataset 5: NO2/NO3 concentration (1x1 km)
    Dataset 6: SO2 concentration (1x1 km)
    - Datasets 1–3: deposition by habitat (forest, moorland, grid-average) at 5x5 km
    - Datasets 7–9: min/max/average deposition per site (forest or moorland) at 5x5 km
    - Datasets 10–12: min/max/average concentrations per site at 1x1 km (NO2/NOx, NH3, SO2)
  - Site-level metadata includes SITECODE, SITENAME, SITEAREA, CENTROID coordinates, DESIGNATION, YEAR, and GRIDAREA.

- Data units and conversions
  - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 via standard multipliers).
  - Concentrations: µg m-3 for NH3, NOx, NO2, SO2.

- Data sources and references
  - UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) and PCM model information and data sources.
  - Supporting information and model evaluation references, with listed URL endpoints for data and model details.

- Practical notes for GIS work
  - Handling data at different resolutions (5x5 km vs 1x1 km) and applying area-weighted calculations within site boundaries.
  - Clipping, merging, and grid-alignment to produce consistent, site-referenced rasters and attribute tables.
  - Documentation of data structure (datasets and fields) essential for reproducibility and further GIS analyses.

- Access and references
  - Key resources include Defra/UK-DEFRA PCM and UKEAP information pages and related deposition data portals (provided URLs in the project notes).