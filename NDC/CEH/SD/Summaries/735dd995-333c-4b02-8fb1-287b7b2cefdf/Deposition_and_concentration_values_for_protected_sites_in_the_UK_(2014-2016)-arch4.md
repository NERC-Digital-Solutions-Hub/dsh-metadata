# CBED Modelling and PCM Modelling for UK Protected Sites: Spatial Mapping and 3-Year Means (2014-2016)

- This document describes an end-to-end data processing workflow to map deposition and pollutant concentrations to UK protected sites (SAC, SPA, SSSI) using two modelling approaches: CBED (Concentration Based Estimated Deposition) and PCM (Pollution Climate Mapping).
- Outputs are prepared at fine spatial resolutions (5x5 km grid for deposition; 1x1 km grid for concentrations) and aligned to boundaries of protected sites.

## Purpose, Scope and Data Sources

- Objective: generate spatially explicit deposition and concentration values for protected sites to assess environmental impact and support policy analysis.
- Data sources and inputs:
  - CBED data: 3-year average deposition for nitrogen and sulphur compounds derived from gas/particle concentrations and precipitation measurements from the UKEAP network.
  - PCM data: 1x1 km grid background concentrations for multiple pollutants, with base-year and projection model runs (DEFRA/Ricardo Energy & Environment).
  - Protected sites: SAC, SPA, and SSSI boundaries obtained from JNCC and country-specific sources.
  - Supporting meteorology: UK Met Office precipitation data; orographic enhancement factors for upland regions.
- Temporal framework: results provided as rolling 3-year means (2014–2016) to smooth inter-annual variability; also generated as annual values where appropriate.

## Step 1: Spatial Mapping of Deposition and Concentration

- Process:
  - Create a UK-wide 5x5 km grid using Feature Manipulation Engine (FME).
  - Clip grid data to the boundaries of UK protected sites (SAC/SPA/SSSI) to produce site-specific gridded datasets.
  - Merge site-specific grids with 3-year CBED outputs to form a UK protected sites CBED dataset.
  - Repeat the same approach for 1x1 km NOx and SO2 concentration datasets from the PCM model.
- Data integration:
  - Boundary and site data (SAC/SPA) from JNCC; SSSI data from national websites.
  - Output: a gridded representation of CBED deposition and PCM concentrations aligned to protected site polygons.

## Step 2: Minimum, Maximum, and Grid-Average Values

- Purpose: derive site-level deposition/concentration metrics using grid data.
- Method:
  - For each protected site, compute grid-square area weights and apply them to the grid-level CBED deposition values to obtain a site-wide grid-average deposition.
  - Calculation example: CBEDDepositionValue × (GridArea / TotalSiteArea), then sum across grids to yield the site average.
- Outputs:
  - For each site, produce minimum, maximum, and grid-average deposition/concentration values (in keq ha-1 year-1 for deposition; in µg m-3 for concentrations).

## CBED Modelling

- What CBED does:
  - Generates 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised and reduced nitrogen, and base cations from interpolated site measurements and precipitation-driven wet deposition.
  - Dry deposition derived from gas/PM concentrations combined with habitat-specific deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
  - Wet deposition combines precipitation data with gas/PM concentrations, including occult (cloud) deposition to vegetation.
- Key features:
  - Habitat-specific deposition applied to ecosystems (moorland vs forest) and grid-average scenarios.
  - Separation of anthropogenic vs total sulphur and calcium using sea-salt indicators.
  - Orographic enhancement incorporated for upland regions.
  - Inter-annual variability acknowledged; results averaged over 3-year periods to provide stable estimates.
- Outputs:
  - 3-year mean CBED deposition values at 5x5 km grid resolution, with ecosystem-specific (moorland/forest) and grid-average scenarios.
  - Datasets cover multiple components: NH3/NH4, NO2/NO3, SO2/SO4, with related wet/dry deposition components.

## PCM Modelling

- What PCM does:
  - Produces background maps and 1x1 km grids of pollutant concentrations for the UK, satisfying EU Directive requirements (2008/50/EC).
  - Separate model runs exist for base year and projections, used for scenario assessment and population exposure calculations and to support policy development.
- Key features:
  - One model per pollutant (e.g., NOx, NO2, PM10, PM2.5, SO2, etc.).
  - Outputs include 1x1 km concentration maps and around 9,000 representative road-side values.
- Outputs:
  - Concentration data on 1x1 km grids and aggregated site-level values consistent with the 3-year rolling average framework.

## Data Outputs, Units and Structure

- Nature and units:
  - Deposition: keq ha-1 year-1 (converted to kg S ha-1 year-1 or kg N ha-1 year-1 as needed by multiplying by 16 or 14, respectively).
  - Concentrations: µg m-3.
- Data structure and datasets (3-year means 2014-2016; additional min/max/grid-averages):
  - Dataset 1-3: 3-year mean ecosystem-specific deposition (forest, moorland, grid-average) at 5x5 km resolution.
  - Dataset 4: Ammonia concentration at 5x5 km grid.
  - Dataset 5: NOx concentration at 1x1 km grid.
  - Dataset 6: SO2 concentration at 1x1 km grid.
  - Dataset 7-9: Minimum, maximum, and average deposition values for forest/moorland across sites at 5x5 km resolution.
  Dataset 10: Minimum, maximum, and average deposition values at grid-average 5x5 km resolution.
  Dataset 11: Ammonia concentration at site level (minimum, maximum, average).
  Dataset 12: NOx concentration at site level (minimum, maximum, average).
  - Additional site- and grid-level metadata fields included (SITECODE, SITENAME, GRIDAREA, YEAR, CENTROID_X/Y, etc.).
- Data quality notes:
  - NaN entries indicate missing data in originating datasets.
  - Datasets inter-relate 5x5 km grid data (CBED) with 1x1 km concentration data (PCM) and site-level aggregations for protected areas.

## Quality Control and governance

- QA practices:
  - Methods aligned with government analytical model QA standards; extensive peer review of CBED data.
  - Involvement in Defra model inter-comparison exercises.
  - Documentation of method developments, version control, and central storage of code.
  - Mass balance checks and cross-year comparisons to ensure numerical consistency.
- Reproducibility and transparency:
  - Clear data structure documentation for each dataset (fields, units, descriptions).
  - References and supporting information cited for model methods and enhancement factors.

## Practical Implications for Data Leaders

- Demonstrates an end-to-end data pipeline from raw measurements to site-specific deposition and concentration metrics, suitable for governance reviews and cross-sector collaboration.
- Emphasizes the importance of:
  - Data discoverability and standardization (consistent units, grid schemes, and site aggregation methods).
  - Metadata richness (site codes, boundary geometry, grid areas, designation types, year, etc.).
  - Robust QA, versioning, and peer-review processes to support policy-relevant modelling.
  - Handling of inter-annual variability via rolling means and explicit treatment of habitat-specific deposition.
- Supports data-driven policy analysis for protected ecosystems and cross-boundary environmental management.