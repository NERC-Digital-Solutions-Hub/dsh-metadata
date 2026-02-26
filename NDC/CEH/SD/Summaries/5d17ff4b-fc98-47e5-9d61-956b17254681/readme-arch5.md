# Topographic change dataset for Antamok River catchment during Typhoon Mangkhut (2018)

## Overview
- Generated from numerical simulations using free software r.avaflow, v2.4 to map topographic change.
- Study area: Antamok River catchment, Itogon, Philippines.
- Event context: Typhoon Mangkhut, 2018.

## Data content and units
- Change in topography of the study area; positive values indicate deposition, negative values indicate erosion.
- Units: metres.

## Quality control and provenance
- Data quality checked against observed channel widening limits using remote sensing observations before and after the Typhoon event.

## Data structure and files
- Test1_N.asc: final topographic change of the Northern part of the catchment.
- Test1_S.asc: final topographic change of the Southern part of the catchment.
- N_3.tif, N_30.tif, N_60.tif, N_180.tif: Northern part topographic change at 3, 30, 60, and 180 seconds respectively.
- S_3.tif, S_30.tif, S_60.tif, S_180.tif: Southern part topographic change at 3, 30, 60, and 180 seconds respectively.

## Coordinate Reference System (CRS)
- EPSG:3124 — PRS92 zone 4.

## Data governance considerations for Data Stewards
- Provenance and method: clearly documented use of r.avaflow v2.4; context of Typhoon Mangkhut 2018.
- Metadata needs: include scope (study area, event), data types, units, file descriptions, temporal points, and QA notes.
- File formats and interoperability: ASC and TIFF formats; maintain consistent naming and documentation to support cross-system use.
- Access, licensing, and sharing: align with repository requirements; specify any restrictions and attribution.
- Maintenance and updates: establish a process for adding new simulations or updated results; document any changes to data or processing.
- Quality assurance: retain validation evidence (remote sensing comparisons) and provide traceability to methods and parameters.