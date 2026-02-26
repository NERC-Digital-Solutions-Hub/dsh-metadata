# Topographic change dataset for Antamok River catchment, Itogon, Philippines during Typhoon Mangkhut, 2018

## Overview
- Data produced via numerical simulations using free software r.avaflow, v2.4 to generate maps of topographic change.
- Study area: Antamok River catchment in Itogon, Philippines.
- Event modeled: Typhoon Mangkhut in 2018.

## Collection/generation methods
- Simulation-based data collection using r.avaflow (v2.4).
- Outputs are maps of topographic change, indicating deposition (positive values) and erosion (negative values).
- Units: meters.

## Quality control
- Data validated against observed channel widening limits using remote sensing observations from before and after the Typhoon event.

## Data structure
- Files included:
  - Test1_N.asc – final topographic change for the Northern part of the catchment
  - Test1_S.asc – final topographic change for the Southern part of the catchment
  - N_3.tif – Northern part after 3 seconds in the simulation
  - N_30.tif – Northern part after 30 seconds
  - N_60.tif – Northern part after 60 seconds
  - N_180.tif – Northern part after 180 seconds
  - S_3.tif – Southern part after 3 seconds
  - S_30.tif – Southern part after 30 seconds
  - S_60.tif – Southern part after 60 seconds
  - S_180.tif – Southern part after 180 seconds

## Coordinate Reference System (CRS)
- EPSG:3124 – PRS92 zone 4

## Notes for data use
- Data formats include ASCII grid (.asc) and GeoTIFF (.tif); topographic change values represent metres of deposition or erosion.
- Suitable for GIS analyses of sediment transport, erosion/deposition patterns, and validation against observed data.
- Clear file naming and time-step organization support comparison and integration with other datasets.