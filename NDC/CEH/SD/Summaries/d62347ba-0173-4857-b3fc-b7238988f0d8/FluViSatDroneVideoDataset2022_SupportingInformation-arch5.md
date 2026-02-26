# Supporting documentation for: Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

## Overview
- Dataset of drone videos intended to validate surface water flow speeds for the FluViSat project (Hydrological Flow Measurement from Satellite Video).
- Covers sites in the UK, Australia, Switzerland and Japan under varied flow conditions.
- Includes fieldwork dates, conditions, and instrumentation context; data hosted with governance and permissions in place.

## Data Content and Formats
- Files: one MP4 video per file; one SRT subtitle file per video (Burdekin and Uono have only MP4s).
- Resolutions: 1080p and 4K MP4s.
- Metadata about recordings embedded in file naming and folder structure.
- No calibration data stored with the videos; scaling performed during processing using manual measurements of static features.

## Data Organization and Metadata
- Site locations and types:
  - Burdekin River, Australia (River) – lat/long provided
  - Falls of Lora, Scotland (Tidal) – lat/long provided
  - River Tweed, UK (River) – lat/long provided
  - Uono River, Japan (River) – lat/long provided
  - Rhine Falls, Switzerland (River) – lat/long provided
- Folder structure: X_YYYYMMDD format, where X is a site code (Burdekin, Lora, Rhine, Tweed, Uono).
- Number of dates per site:
  - Burdekin: 3 dates
  - Falls Of Lora: 5 dates
  - Rhine at Rhine Falls: 1 date
  - Tweed: 1 date
  - Uono: 1 date (two locations 1 km apart: Negoya Bridge and Horinouchi)
- File naming: DJI_ref_X_DDMM2022 (drone type, image ref, site, date).

## Collection Methods and Instrumentation
- Drone platform: standard unmodified DJI Air 2S.
- Collection method: nadir-view videos hovered over the water center to capture full width.
- Flight parameters: short clips of 20–30 seconds; altitude chosen to optimize imagery for both drone and satellite velocimetry processing.
- Additional field instruments (not part of the dataset):
  - Laser distance meters
  - Boats-mounted Acoustic Doppler Current Profiler (ADCP)
- Compliance: drone operations conducted under country regulations with required permissions where applicable.

## Quality Assurance and Provenance
- Quality control: camera settings optimized for stable, sharp, well-lit footage; independent river width observations used to verify video-derived results.
- Author contributions: N. Everard (primary author; main contact) and M. Randall (video collection for Burdekin and Uono; methodology expert).
- Funding and hosting: Future-EO-1 EO Science for Society; funded by the European Space Agency; data housed in the NERC Environmental Information Data Centre (EIDC).

## Data Access, Governance and Usage
- Data governance: follows standards appropriate for large datasets with clear provenance and site-specific metadata.
- Access: data are stored at the NERC Environmental Information Data Centre; licensing and reuse terms are not specified in the document and should be confirmed with the data centre.
- Usage notes:
  - No calibration data included; scaling performed during processing via manual feature measurements.
  - ADCP and other field data used for context are not provided with the dataset.

## Site Information and Coordinates
- Australia – Burdekin River (River) – lat/long: -20.628567, 147.165902
- UK – Falls Of Lora (Tidal) – lat/long: 56.456156, -5.393815
- UK – River Tweed (River) – lat/long: 55.722825, -2.162671
- Japan – Uono River (River) – lat/long: 37.2458506, 138.9275143
- Switzerland – River Rhine at Rhine Falls (River) – lat/long: 47.674231, 8.609999

## Contact and Documentation
- Primary contact: N. Everard (data custodian and point of contact)
- Co-contributor: M. Randall (video collection and methodological expert)