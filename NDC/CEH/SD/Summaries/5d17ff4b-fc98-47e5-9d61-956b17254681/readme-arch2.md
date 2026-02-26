Topographic change of the Antamok River catchment during Typhoon Mangkhut (2018) — Simulation results using r.avaflow v2.4

- Overview
  - Uses numerical simulations to produce maps of topographic change for the Antamok River catchment in Itogon, Philippines, during Typhoon Mangkhut in 2018.
  - Aims to demonstrate environmental change in a consistent, monitorable format.

- Data collection and methods
  - Collection/generation via r.avaflow (free software), v2.4.
  - Outputs are maps showing topographic change (deposition: positive values; erosion: negative values).

- Measurement units
  - Change in topography is expressed in metres.

- Quality control
  - Data validated by comparing simulated results with observed channel widening from remote sensing before and after the Typhoon event.

- Data structure and files
  - Test1_N.asc: final topographic change for the Northern part of the catchment.
  - Test1_S.asc: final topographic change for the Southern part of the catchment.
  - N_3.tif, N_30.tif, N_60.tif, N_180.tif: Northern part topographic change at 3, 30, 60, and 180 seconds in the simulation.
  - S_3.tif, S_30.tif, S_60.tif, S_180.tif: Southern part topographic change at 3, 30, 60, and 180 seconds in the simulation.

- Coordinate Reference System (CRS)
  - EPSG:3124 - PRS92 zone 4.

- Relevance for environmental monitoring
  - Provides standardized environmental-change outputs suitable for monitoring and policy evaluation over time.
  - The clearly named, time-stamped raster files facilitate comparison and trend analysis across the study area.
  - Designed to be stored and uploaded to appropriate data portals, aligning with best practices for dataset accessibility.

- Practical applications and integration
  - Supports hazard assessment and landform change analysis due to extreme weather events.
  - Can be combined with other datasets (e.g., remote sensing, rainfall, land use) to enhance data value and enable broader analyses.
  - Encourages open access to underlying simulation outputs to support transparency and reuse.