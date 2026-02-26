# Supporting documentation for:
Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

## Overview
- Purpose: Provide field validation of surface water flow speeds derived from satellite video for the FluViSat project (Hydrological Flow Measurement from Satellite Video).
- Scope: Drone video footage from five sites across the UK, Australia, Switzerland, and Japan, captured under varying flow conditions.
- Funding and governance: Conducted under Future-EO-1 EO Science for Society and funded by the European Space Agency (ESA).

## Fieldwork instrumentation
- Drones: Standard, unmodified DJI Air 2S consumer cameras.
- Additional field instruments (not included in the dataset): laser distance meters and boats equipped with Acoustic Doppler Current Profiler (ADCP).
- Compliance: Operations conducted in accordance with country drone regulations and required permissions.

## Collection method
- Video type: Nadir-view MP4 videos captured over the center of the flowing water to cover full width.
- Altitude and framing: Altitude chosen to capture full water width; pre-flight calibration not required beyond standard checks.
- Video length: Each clip is between 20 and 30 seconds.

## Experimental design / Sampling regime
- Site selection: Chosen for favorable flow and surface conditions for both drone and satellite velocimetry, with safety and practicality considered.
- Repetition: Multiple videos per site on different dates to capture varying flow conditions.

## Quality Control
- Video quality: Drone camera settings optimized for stable, sharp, well-lit, correctly exposed footage.
- Validation: Independent observations of river width used to verify results from processed videos.

## Nature and units of recorded values
- Data types: MP4 video files (1080p and 4K) and corresponding SRT subtitle files; Burdekin and Uono datasets contain only MP4 files.
- Calibration: No pre-flight calibration; scaling/calibration performed during processing using identifiable static features in the imagery.

## Site locations
- Australia – Burdekin River (River): -20.628567, 147.165902
- UK – Falls of Lora (Tidal): 56.456156, -5.393815
- UK – River Tweed (River): 55.722825, -2.162671
- Japan – Uono River (River): 37.2458506, 138.9275143
- Switzerland – Rhine Falls (River): 47.674231, 8.609999

## Data structure
- Organization: Data files organized into folders by site and date using the format X_YYYYMMDD (X = site code).
  - Burdekin (Burdekin) – 3 dates
  - Falls Of Lora (Lora) – 5 dates
  - River Rhine at Rhine Falls (Rhine) – 1 date
  - River Tweed (Tweed) – 1 date
  - Uono River (Uono) – 1 date (two locations 1 km apart: Negoya Bridge ref=1 and Horinouchi ref=2)
- File naming: DJI_ref_X_DDMM2022 (DJI = drone type, ref = image ref, X = site, DDMM = date)
- Contents per folder: Video files (MP4) and optional subtitles (SRT); Uono and Burdekin exclude SRT.

## Author contributions
- N. Everard: Primary author and contact for the data.
- M. Randall: Collected Burdekin videos and provided Uono videos; expert on the methodology.

## Relevance for monitoring frameworks
- Uses: Provides ground-truth video datasets to validate satellite-derived surface velocity measurements, aiding policy and decision-making in environmental monitoring.
- Data quality and governance:
  - Clear documentation of instruments, methods, and validation steps (independent width checks).
  - Well-structured metadata: site codes, dates, approximate coordinates, and file naming conventions.
  - Calibration occurs during processing rather than pre-flight, highlighting a data processing step for scale.
- Data accessibility considerations:
  - Field instrumentation data (e.g., ADCP, laser meters) are not included in the dataset; only video data and optional subtitles are provided.
  - Datasets are organized for traceability by site and date, supporting reproducibility and auditability.
- Limitations and challenges for monitoring teams:
  - Location coordinates are approximate.
  - Some metadata (e.g., pre-flight calibration specifics, full ancillary measurements) are not included, which may affect data integration with other datasets.
  - Need to manage data sharing and provenance when combining with other monitoring data sources.