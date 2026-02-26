# Supporting documentation for: Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

## Overview
- Dataset of drone videos intended to calculate surface water flow speeds (velocity) for field validation of satellite-derived velocimetry under the FluViSat project (Hydrological Flow Measurement from Satellite Video).
- Sites and flow conditions include Burdekin River (Australia, high flow), River Tweed (UK, medium), Falls of Lora (UK, tidal, ebb), Uono River (Japan, medium-high), and Rhine Falls (Switzerland, low to medium).
- All footage collected in compliance with country drone regulations and required permissions; funded by the European Space Agency and conducted under Future-EO-1 EO Science for Society.

## Fieldwork instrumentation
- Primary equipment: standard, unmodified DJI Air 2S consumer-grade drones.
- Additional field instruments used to support calculations (not included in dataset): laser distance meters (river width) and boats-mounted ADCP for velocity measurements.
  
## Collection method
- Nadir-view videos captured by hovering over the center of the flowing water to cover the full width.

## Experimental design / Sampling regime
- Video length: 20–30 seconds per recording.
- Site/date selection aimed at favorable flow and surface conditions and ensured safety.

## Quality Control
- Drone camera settings optimized for stable, sharply focused, well-lit, correctly exposed footage.
- Independent river width measurements used to verify results from the processed videos.

## Nature and units of recorded values
- Video files: MP4 in 1080p or 4K resolutions.
- No pre-flight calibration required; scaling performed during processing using manual measurements of distances between identifiable static features.

## Site locations
- Australia: Burdekin River (River) — -20.628567, 147.165902
- United Kingdom: Falls Of Lora (Tidal) — 56.456156, -5.393815
- United Kingdom: River Tweed (River) — 55.722825, -2.162671
- Japan: Uono River (River) — 37.2458506, 138.9275143
- Switzerland: Rhine Falls (River) — 47.674231, 8.609999

## Data structure
- Each video has one MP4 and one SRT file, except Burdekin and Uono (only MP4s provided).
- Files organized in folders by site and date using the format X_YYYYMMDD (X = site code: Burdekin, Lora, Rhine, Tweed, Uono).
- Filenames follow: DJI_ref_X_DDMM2022 (drone type, reference, site code, date).
- Uono River videos collected at two locations 1 km apart: Negoya Bridge (ref=1) and Horinouchi (ref=2).

## Site codes and dates
- Burdekin River: 3 dates
- Falls Of Lora: 5 dates
- Rhine Rhine Falls: 1 date
- Tweed: 1 date
- Uono: 1 date

## Author contributions
- N. Everard: primary author and data contact.
- M. Randall: collected Burdekin videos and contributed Uono footage; methodology expert.

## Funding and permissions
- Funded by the European Space Agency; project context: Future-EO-1 EO Science for Society.
- Compliance with drone regulations and permissions as required.