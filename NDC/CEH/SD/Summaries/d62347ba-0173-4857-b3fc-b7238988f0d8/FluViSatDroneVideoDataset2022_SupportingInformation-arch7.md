# Supporting documentation for: Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

## Overview
- A dataset of drone videos used to calculate surface water flow speeds (velocity) for field validation of satellite-derived video velocimetry within the FluViSat project (Hydrological Flow Measurement from Satellite Video).
- Sites span the UK, Australia, Switzerland, and Japan, with footage captured under varied flow conditions.
- Data collected under Future-EO-1 EO Science for Society and funded by the European Space Agency (ESA).
- All footage obtained in compliance with local drone regulations and permissions where required.

## Fieldwork instrumentation
- Primary equipment: standard DJI Air 2S drones (unmodified) for nadir-view video.
- Additional field instruments (not included in dataset): laser distance meters for river width measurements and boats-mounted ADCP for flow speed measurements.
  
## Collection method
- Nadir-view videos hovered over the center of the flowing water to capture full width.
- Video durations: 20–30 seconds per recording.
- Sites selected for favorable drift and surface conditions for both drone and satellite velocimetry processing, with safety and practicality in mind.

## Experimental design / Sampling regime
- Multiple videos per site on different dates; sites chosen to cover a range of flow conditions.
- Dates and observed conditions noted for each site (e.g., high, medium, low flow).

## Quality Control
- Drone camera settings optimized for stable, sharply focused, well-lit, properly exposed surface footage.
- Independent observations of river width performed to verify results from processed videos.

## Nature and units of recorded values
- Video files: MP4, in 1080P (1080 x 1920) and 4K (2160 x 3840) resolutions.
- Subtitles: SRT files accompany most videos (Burdekin and Uono are provided as MP4 only).
- Calibration: No preflight calibration required; scaling calibrations performed during processing using measurements of identifiable static features.

## Site locations
- Australia – Burdekin River (River): -20.628567, 147.165902
- United Kingdom – Falls Of Lora (Tidal): 56.456156, -5.393815
- United Kingdom – River Tweed (River): 55.722825, -2.162671
- Japan – Uono River (River): 37.2458506, 138.9275143
- Switzerland – River Rhine at Rhine Falls (River): 47.674231, 8.609999

## Data structure
- Each video folder contains one MP4 plus an SRT file (except Burdekin and Uono, which include only MP4).
- Folders are organized by site and date using the format: X_YYYYMMDD (X = site code).
- Site codes and date counts:
  - Burdekin River — code: Burdekin — 3 dates
  - Falls Of Lora — code: Lora — 5 dates
  - River Rhine at Rhine Falls — code: Rhine — 1 date
  - River Tweed — code: Tweed — 1 date
  - Uono River — code: Uono — 1 date
- File naming (example): DJI_ref_X_DDMM2022 (DJI = drone type; ref = image ref; X = site; DDMM = day and month). Uono data include two locations 1 km apart: Negoya Bridge (ref=1) and Horinouchi (ref=2).

## Author contributions
- N. Everard: primary author and contact for the data.
- M. Randall: collected Burdekin videos and provided Uono footage; expert on methodology.

## GIS relevance and potential uses
- Provides ground-truth video data for validating satellite-derived surface flow measurements.
- Location metadata enables mapping of study sites and integration with other GIS layers (basemaps, hydrology, river networks).
- Video and associated SRT (where available) can be used to derive velocity fields and cross-validate raster-based flow estimates within GIS workflows.
- Data structure supports organizing and linking imagery to site attributes, aiding reproducibility and traceability in GIS analyses.