# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

- This document describes the UK Saltmarsh Monitoring Project dataset, including methods, structure, and metadata to support GIS-based analysis and map visualisation.

## Overview of the Dataset

- Measures sediment elevation using Surface Elevation Tables (SET) and marker horizons, plus environmental metadata (soil composition, plant cover, installation details such as rSET depth).
- Field sites span UK coastlines from North Scotland to the South Coast of England, across 16 saltmarshes (e.g., Dornoch Point, Campfield Marsh, Warton Marsh, Brancaster, Blakeney, Gutner Point, West Itchenor, Pilsey/Thorney Island, etc.).
- Observations linked by unique plot codes (e.g., SET1_RBMS) and metadata CSVs to allow cross-referencing between measurements and site context.

## Spatial Coverage

- 16 marshes across multiple estuary groups:
  - Dornoch Firth (DFDP)
  - Solway (SWCB, SWCV, SWCF)
  - Ribble (RBWM, RBBS, RBMS)
  - North Norfolk (NNSK, NNBB, NNBN)
  - Wash (WSWM, WSBE, WSBW)
  - Solent (CHWI, CHPS, CHGP)
- Exact plot locations captured with GPS; elevation estimates also derived from LIDAR data and GNSS measurements.
- Appendix 2 provides locations and coordinates for all SET bases (e.g., RBMS1–RBMS3, RBBS1–RBBS3, DFDP1–DFDP3, etc.).

## Temporal Coverage

- Initial measurements in spring/summer 2023.
- Follow-up monitoring in spring and autumn 2024.
- LIDAR elevation data year recorded; annual monitoring planned (spring) with autumn monitoring when possible.

## Data Collection and Methods

- Primary method: SET-MH (Surface Elevation Table - Marker Horizon) for elevation and accretion measurements.
- Installation methodology:
  - SET bases installed following Lynch et al. 2015 protocol.
  - Three SET plots per marsh at similar elevation and mid-marsh plant communities; 5 m from creek edge.
  - External edge marked with 50 x 50 cm quadrats; feldspar clay marks applied to create standard horizon for marker measurements.
- Replication and controls:
  - Elevation measurements: nine pins across multiple orientations (initially eight; later nine).
  - Marker horizons: triplicate measurements from at least three plots.
  - Plant community monitored via DAFOR scale and National Vegetation Classification (NVC) codes; elevation estimated also from LIDAR and GNSS.
- Periodicity and sampling:
  - Annual data collection in spring; occasional autumn monitoring.
  - 4104 elevation observations across 48 SETs from 16 marshes.

## Data Structure and Files

- Four main CSV data files:
  - 08318setmhsitemetadata.csv: site-related metadata (location, coordinates, depth of rSET, LIDAR year/elevation, GNSS elevation, vegetation codes, weather/sediment observations).
  - 08318setmhsamplingmetadata.csv: sampling-related metadata (row numbers, timestamps, SET IDs, photos, dominant/abundant/frequent/occasional/rare species with NVC codes, notes).
  - 08318setdata.csv: elevation measurements (per pin/orientation, per plot), including location code, plot code, replicate, timestamps, orientation, height of pins, and notes.
  - 08318mhdata.csv: marker horizon measurements (depth to horizon, per pin/core, timestamps, orientation, notes).
- Data structure details:
  - Location codes link sites to site descriptions and coordinates.
  - plot_code follows the format SETnumber_LocationCode (e.g., SET1_RBMS).
  - replicate_code distinguishes readings by pin numbers (1-9) and cores for marker horizons.
  - timestamp_T0 and timestamp_TN indicate reference and reading dates.
- Variable and coding details:
  - Geographic coordinates in decimal degrees (Latitude, Longitude).
  - Depth of rSET in meters; elevations from GNSS and LIDAR in meters.
  - Plant community data encoded using Dominant/Abundant/Frequent/Occasional/Rare with species codes (e.g., Ap = Atriplex prostrata).
  - NVC codes accompanying vegetation classifications.
  - Instrument: UKCEH R-SET; notes capture weather, site, sediment, installation observations.
- Appendices:
  - Appendix 1: NVC saltmarsh community floristic tables (e.g., SM13a, SM14a, SM16a sub-communities).
  - Appendix 2: Locations and coordinates of all SET bases.

## Data Quality, Calibration, and Processing

- Calibration:
  - Instruments calibrated per manufacturer specifications.
  - LIDAR-based elevation estimates used in conjunction with GNSS measurements; year of LIDAR data recorded.
- Quality control:
  - Photographs of each plot; metadata and data reformatted and linked via unique IDs.
- Processing and analysis:
  - Future analyses planned in R; accompanying scripts expected in future publications.
  - GIS-ready linking of measurements to site metadata, horizons, and vegetation context via unique IDs.

## References and Appendices

- Reference protocol: Lynch, J. C., Hensel, P., & Cahoon, D. R. (2015) – The surface elevation table and marker horizon technique.
- Appendices include NVC community tables and SET base locations with coordinates recorded in the dataset.

## Practical Notes for GIS Specialists

- Four CSVs provide a complete, joinable dataset: site metadata, sampling metadata, rSET elevation data, and marker horizon data.
- Spatial precision combines GNSS point elevations with LIDAR-derived elevations; ensure consistent CRS when integrating into GIS workflows.
- Plot and SITE identifiers (location_code, SET_ID, plot_code) enable efficient cross-linking of measurements with environmental context (vegetation codes, sediment notes, weather conditions).
- Vegetation and NVC codes are important for habitat classification analyses and potential stratification in map visualisations.
- Appendix 2 provides concrete coordinates for SET bases, useful for plotting sampling locations and generating spatial analyses or basemaps.

## Contact and Access

- Enquiries: enquiries@ceh.ac.uk
- Organisations: UK Centre for Ecology & Hydrology (CEH) – Bangor, Edinburgh, Lancaster, Wallingford.