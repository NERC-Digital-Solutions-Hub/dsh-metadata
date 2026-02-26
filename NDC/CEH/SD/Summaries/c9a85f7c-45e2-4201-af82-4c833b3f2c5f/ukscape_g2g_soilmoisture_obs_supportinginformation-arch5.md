# Supporting information for Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by observed data (1980 to 2011)

- Purpose and scope
  - Provides documentation for Grid-to-Grid (G2G) soil moisture estimates driven by observed meteorological data for GB and NI (1980–2011).
  - Part of UK-SCAPE (UK Status, Change And Projections of the Environment) research on climate-change impacts on water quantity; complements UKCP18-driven datasets (1980–2080) and related river-flow datasets.

- Data content and outputs
  - G2G model outputs: monthly mean soil moisture content (m water/m soil) on a 1 km × 1 km grid across GB and NI.
  - Outputs are provided as gridded, spatially-consistent estimates of natural river flows and soil moisture; precipitation and potential evaporation drive the model.
  - Complementary datasets include G2G outputs driven by UKCP18 regional climate projections and related river-flow datasets (GB and NI).
  - Additional spatial aids: 1 km × 1 km lake identification grids for GB and NI; lakes are not modeled explicitly for storage or regulation.

- Model and inputs
  - Hydrological model: Grid-to-Grid (G2G), a national-scale grid-based model (1 km × 1 km; 15-minute time-step for GB; extended to NI and some Ireland drainages).
  - Inputs required: daily precipitation (1 km, CEH-GEAR), monthly potential evaporation for short grass (MORECS, 1 km), daily min/max temperature (1 km, Met Office).
  - Snow module available but optional; temperature data downscaled to daily values via sine curves.
  - Model uses spatially varying soil properties (depth variability) but does not calibrate parameters for individual catchments; urban areas influence captured via runoff, while lakes/reservoirs and abstractions are not modeled.
  - Output interpretation: soil moisture represents depth-integrated soil moisture for the whole soil column; 0–1 range corresponds to volumetric content (θ).

- Spatial and temporal coverage
  - Temporal extent: 1980–2011 (monthly means provided).
  - Spatial domain: GB (700 km × 1000 km domain) and NI (187 km × 170 km domain) aligned to the GB national grid; includes grid cells overlapping lakes (lake cells included in the dataset).

- Data format and organization
  - Primary data format: NetCDF4.
  - GB file: G2G_GB_mmsoil_obs_1980_2011.nc (monthly mean soil moisture, Dec 1980–Nov 2011).
  - NI file: G2G_NI_mmsoil_obs_1980_2011.nc (monthly mean soil moisture, Dec 1980–Nov 2011).
  - Time reference: days since 1900-01-01; monthly values assigned to the first day of each month.
  - Lake grids: separate files identifying majority lake cells:
    - GB: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc
    - NI: UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
  - Lake grid encoding: land = 1, lake = 2, sea = -9999; derived from Land Cover Map 2015 data (>=85% water for lake designation).

- Data quality, limitations, and caveats
  - Lakes and reservoirs not explicitly modeled for storage or downstream regulation; lake cells are treated as rivers for downstream interpretation.
  - G2G performance: calibrates best for natural-flow-dominated catchments with accurate flow records; less accurate where artificial abstractions/discharges or complex subsurface hydrology occur.
  - No per-catchment parameter calibration; some non-interoperable, bespoke approaches may be required for certain data scenarios.
  - Units and interpretation: soil moisture is a depth-integrated value; context is needed when comparing to soil layers or depth-specific measurements.

- Use cases and interoperability
  - Can be analyzed alongside UKCP18-driven soil moisture datasets (1980–2080) and UK-SCAPE river-flow datasets.
  - Serves as historical context to MaRIUS-G2G-MORECS-monthly soil moisture datasets (an update with differences in period, land-sea mask, and missing data infilling).
  - Suitable for assessing climate-change impacts on soil moisture and for supporting hydrological or water-resource studies at national (GB/NI) scales.

- Metadata, provenance, and documentation
  - Acknowledgement: funded by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE National Capability.
  - Documentation references include foundational papers and data sources for inputs (CEH-GEAR, MORECS, Met Office HadUK-Grid) and related hydrological modeling work.
  - Related datasets and DOIs are provided to facilitate cross-linking with river flow data and climate-projection-driven soil moisture products.

- Access, licensing, and reuse notes
  - Data are distributed via the NERC Environmental Information Centre (EIDC) with DOIs available for the associated datasets and documents.
  - Descriptions and conventions follow UKCEH gridded dataset standards; file naming and structure are standardized for GB and NI.

- Related datasets and references
  - UK-SCAPE and MaRIUS-G2G-MORECS-monthly datasets for comparative soil moisture products.
  - UKCP18 12 km regional projections dataset and corresponding soil-moisture/river-flow datasets for GB and NI.
  - Foundational modeling and data sources: CEH-GEAR, MORECS, Met Office HadUK-Grid, and Land Cover Map 2015 for lake identification.