# SOC-D: Soil Organic Carbon Dynamics

- A comprehensive data suite describing aboveground and belowground measurements across five grassland-to-woodland contrasts in England (2018–2021) to understand soil organic carbon (SOC) dynamics.
- Aims to test biotic/abiotic controls on SOC stability, identify at-risk areas, and inform land management policies to enhance SOC storage.
- Data are designed for GIS-based visualization and spatial analysis, with explicit site locations, grid layouts, and co-located measurements across multiple depths and soil properties.

## What the dataset contains (GIS-relevant data products)

- Co-located measurements at five long-term grassland-to-woodland contrasts (England):
  - Aboveground net primary productivity (ANPP)
  - Litter layer depth
  - Soil chemical, physical, and biological properties (0–100 cm, up to six depth increments)
  - Soil hydraulic conditions (soil water release curves and unsaturated hydraulic conductivity)
  - Earthworm counts and species
- Datasets are organized to support map-based exploration and cross-dataset joins:
  - Co-location and location metadata file
  - ANPP estimates and litter depth
  - Soil physical/chemical/biological properties (0–1 m)
  - Soil hydraulic conductivity and HYPROP raw data
  - Earthworm counts and species identifications
  - Microbial sequence data (amplicons and metagenomes) with derived metrics
- Spatial references and linking keys:
  - Location IDs connect all measurements to site metadata
  - OS grid references and latitude/longitude coordinates (OSGB36 and WGS84)
  - Grid layout and transition boundary between grassland and woodland
  - Precise sampling points within grids (Grid 1–6; Plot 1 grassland, Plot 2 woodland)

## Spatial design and site layout (GIS perspective)

- Five contrasts across England:
  - Gisburn-1, Gisburn-2 (North England)
  - Alice Holt (South England)
  - Wytham Woods (South England)
  - Kielder Forest (North England)
- Each contrast includes two plots (grassland vs woodland) and nine sampling locations per plot, with grids 1–3 in grassland and 4–6 in woodland.
- The contrast boundary lies between grids 3 and 4; sampling points are randomized within grids, with additional location descriptors:
  - Transition distance from boundary
  - Lateral distance from grid edge
- Spatial data accompany field maps, supplementary figures, and GIS-ready coordinates (OS grid references, latitude/longitude).

## Datasets and data structure (how to join and use)

- Connector and location metadata
  - SOC-D_DATABASE_CONNECTOR.csv: enables linking sample IDs to site, plot, grid, core, and spatial geometry (transition and lateral distances)
  - SOC-D_DATABASE_LOCATIONS.csv: site IDs, grid references, and coordinates (OS grid, lat/long)
- Aboveground and litter data
  - SOC-D_DATABASE_ANPP.csv: ANPP estimates (mean, high/low bounds) linked to LOCATION_ID
  - SOC-D_DATABASE_LITTER_DEPTH.csv: litter depth (mean of three measurements) linked to LOCATION_ID
- Soil metrics (0–1 m)
  - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv: core-level soil metrics (bulk density, pH, EC, LOI, total C/N, etc.)
  - SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: grid-specific soil metrics for grassland (grid 2) and woodland (grid 5), including mineral soil fractions and enzyme metrics
  - SOC-D_DATABASE_SOIL_METRICS_TOP_AND_SUB_SOIL.csv: top and subsoil metrics (0–15 cm and below 50 cm) for all grids
- Soil hydraulic properties
  - SOC-D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv: unsaturated hydraulic conductivity (Kfs) by location
  - HYPROP raw data files: HYPROP measurements and retention data (PF, water content, etc.)
  - HYPROP conductivity data (log10 K) versions
- Earthworms
  - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts by species, fresh biomass, and notes
- Microbial data
  - Amplicon and metagenome results for prokaryotes and fungi
  - Derived ordination scores (nMDS) and community composition metrics
- Data linking
  - SOC-D_DATABASE_CONNECTOR.csv includes SITE_NAME, LANDUSE, GRID, CORE, TRANSITION_DISTANCE, LATERAL_DISTANCE, SLICE, and sampling IDs
  - SOC-D_DATABASE_LOCATIONS.csv provides LOCATION_ID, GRID_REFERENCE, X/Y, latitude/longitude
- File-level notes
  - Missing values are NA; not all measurements are complete at every site/plot
  - Some measurements were not collected at certain sites (e.g., HYPROP cores at Alice Holt), and certain enzyme data were excluded due to field issues

## Key spatial and attribute considerations for GIS work

- Coordinate systems and references
  - Location coordinates include OSGB36 grid references and WGS84 latitude/longitude
  - Enables map-backed analysis and cross-wac with national soil datasets (UKCEH/LUCAS/GMEP/ERAMMP)
- Depth and layer definitions
  - Soil cores are sliced into standard depth increments (e.g., 0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm)
  - Topsoil vs subsoil distinctions are defined for compatibility with national soil datasets
- Spatial sampling design
  - Sampling along transects oriented with respect to the grassland-woodland boundary to capture potential edge effects
  - Grid-level sampling points and transition distance data support neighborhood-scale analyses around the boundary
- Data integration readiness
  - Two linking CSVs (CONNECTOR and LOCATIONS) provide a robust basis for joining ANPP, litter depth, soil metrics, hydraulics, earthworms, and microbial data by site, plot, grid, and core
  - Spatial analyses can compute SOC-related stocks by depth, site, land-use contrast, and grid position

## Data quality, completeness, and caveats

- Completeness
  - Common measurements (LOI, bulk density, pH, EC) are complete; some measurements (e.g., specific soil fractions, certain enzymes, CUE, microbial biomass proxies) are partial or NA for some sites
  - HYPROP cores were not collected at Alice Holt; some earthworm and HYPROP data are missing or incomplete by site
- Quality control
  - Lab QA includes internal standards, calibration checks, replicates (10%), and cross-site references
  - Documentation and supplementary files describe core lengths, hole depths, and coring methods to assess potential compaction effects
- Temporal coverage
  - Sampling occurred 2018–2019 for core collection; additional measurements through 2020–2021 for some parameters (e.g., ANPP, infiltration, earthworms)

## How GIS specialists can use this data

- Build SOC-focused maps
  - Visualize SOC-related pools (LP/OP/MA fractions), carbon/nitrogen content, and dissolved organic carbon across depths and grids
- Analyze spatial drivers of SOC dynamics
  - Explore relationships between SOC metrics and land-use contrast (grassland vs woodland), soil type, and hydrological properties
- Link SOC with soil physics/biology
  - Integrate bulk density, porosity proxies, pH, EC, CEC, and enzyme activities to model SOC stabilization mechanisms across sites
- Cross-dataset analyses
  - Use the Connector and Location files to join ANPP, litter depth, soil properties, hydraulics, earthworms, and microbial metrics for pooled or site-specific studies
- Prepare inputs for process-based models
  - Combine depth-resolved SOC indicators with hydraulic properties and microbial community data to parameterize SOC dynamics models in GIS workflows
- Quality-aware mapping
  - Account for NA values and site-specific data limitations when building SOC stock estimates or risk maps

## Summary of the program and context

- Project: Soil Organic Carbon Dynamics (SOC-D) under the UK-SCAPE programme (NE/R016429/1)
- Purpose: Test how biotic and abiotic soil controls, including structure and biology, govern SOC dynamics across UK land-use gradients; identify at-risk areas and policy-relevant management options
- Scope: Five grassland-to-woodland contrasts across England, with extensive soil, plant, hydrological, earthworm, and microbial data, designed for modular, process-based SOC modelling and national-scale extrapolation