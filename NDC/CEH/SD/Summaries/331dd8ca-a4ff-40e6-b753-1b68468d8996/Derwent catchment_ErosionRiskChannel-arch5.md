# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Overview
- Addresses fine-grained sediment (diffuse pollution) in the River Derwent, Yorkshire.
- Uses SCIMAP to model erosion risk with seasonal variation and multiple scenarios, including bare land detection via satellite and future climate projections.
- Demonstrates how erosion risk changes under different land-use representations, rainfall inputs, drainage inclusion, and UKCP09 climate projections (winter only).

## Data inputs and scenarios (SCIMAP-based)
- Core inputs required by SCIMAP:
  - Elevation: 5 m Ordnance Survey Digital Elevation Model (DEM)
  - Rainfall: monthly Met Office data (2016), long-term average rainfall, or UKCP09 projections
  - Land use: traditional CEH 2015 land use map or seasonal satellite-derived land use (Sentinel-2)
- Scenarios and data configurations:
  - 1) Traditional land use map (CEH 2015), 5 m DEM, 2016 monthly rainfall
  - 2) Seasonal satellite-derived land use (can show bare land), 5 m DEM, 2016 monthly rainfall
  - 3) Long-term rainfall averages, land use from Sentinel-2, 5 m DEM, monthly long-term rainfall
  - 4) Artificial drainage network integrated, Sentinel-2 land use, 5 m DEM, monthly rainfall
  - 5–13) Winter climate change scenarios using UKCP09 data, with:
    - Land use from Sentinel-2, 5 m DEM, artificial drainage network
    - Rainfall projections for High/Medium/Low emissions, across 90th/50th/10th percentiles
    - Winter-only model run (tests for winter conditions)
- Data coverage: seasonal erosion risk mapped for Summer, Spring, Autumn, and Winter across all scenarios.

## Nature, units, and interpretation of values
- Erosion risk values range from 0 to 1, where 1 indicates the highest relative risk within the analysed catchment.
- Output is relative risk (not absolute probability) for comparative interpretation across scenarios and seasons.

## Data structure and presentation notes
- Data are organized by season (Summer, Spring, Autumn, Winter) and by scenario (1–13).
- Shapefiles use graduated colour schemes; when displaying, increase the sampling size in the layer properties to show all data.

## Data provenance and metadata considerations for Data Stewards
- Source and method: SCIMAP-based modelling with explicit inputs (DEM, rainfall, land use) and scenario configurations.
- Scenario metadata to capture:
  - Land-use representation (traditional vs. Sentinel-2 derived)
  - Rainfall input (2016 monthly, long-term average, or UKCP09 projections with emission scenario and percentile)
  - Drainage network inclusion
  - Climate-change scenario details (High/Medium/Low emissions; 90th/50th/10th percentile; winter only)
- Outputs: seasonal erosion risk rasters/shapefiles with values 0–1; need cataloging with season, scenario, inputs, and date/version.
- Documentation needs: maintain traceability of input data sources (CEH, Sentinel-2, Met Office rainfall, UKCP09) and SCIMAP configuration.

## Data quality, limitations, and considerations for reuse
- Outputs are relative risk measures, suitable for comparing scenarios and seasons within the Derwent catchment but not as absolute erosion probabilities.
- Climate projections are limited to winter runs; applicability to other seasons is not covered.
- Shapefile visualization requires appropriate symbol sizing to accurately render all data.
- Users should be aware of potential differences in land-use representation and rainfall inputs when comparing scenarios.

## Data sharing and governance considerations
- Ensure datasets are stored with clear versioning, provenance, and licensing to support discoverability and reuse.
- Upload and catalogue datasets to relevant portals, ensuring metadata captures the SCIMAP-based methodology, inputs, scenario details, and seasonal breakdown.