# Topographic change dataset for Antamok River catchment, Itogon, Philippines during Typhoon Mangkhut (2018) generated with r.avaflow v2.4

## Overview
- Dataset of topographic change (deposition = positive; erosion = negative) for Antamok River catchment in Itogon, Philippines, during Typhoon Mangkhut (2018).
- Generated via numerical simulations using free software r.avaflow v2.4; outputs maps of topographic change.

## Data content and structure
- Data files:
  - Test1_N.asc: final topographic change of the Northern part of the catchment
  - Test1_S.asc: final topographic change of the Southern part of the catchment
  - N_3.tif, N_30.tif, N_60.tif, N_180.tif: Northern part at 3, 30, 60, and 180 seconds
  - S_3.tif, S_30.tif, S_60.tif, S_180.tif: Southern part at 3, 30, 60, and 180 seconds
- Units: metres
- Interpretation: positive values indicate deposition; negative values indicate erosion
- Data formats: ASCII grids (.asc) and GeoTIFF rasters (.tif)

## Quality control
- Validated against observed channel widening limits using remote sensing observations before and after the Typhoon event.

## Coordinate Reference System
- EPSG:3124 — PRS92 zone 4

## Study context
- Location: Antamok River catchment, Itogon area, Philippines
- Event: Typhoon Mangkhut, 2018

## Data governance and usefulness for leadership
- Clear file naming and structure support discoverability and reuse across teams.
- Explicit metadata elements (units, interpretation, CRS) facilitate data integration and cross-team collaboration.
- Quality control aligns simulated outputs with observed changes, supporting credible data-driven decisions.
- Accessible formats (ASCII and GeoTIFF) aid interoperability with common GIS and analysis workflows.