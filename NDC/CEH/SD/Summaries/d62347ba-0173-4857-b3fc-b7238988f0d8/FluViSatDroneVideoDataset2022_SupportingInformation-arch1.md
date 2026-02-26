# Supporting documentation for: Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

## Objective and context
- Drone video dataset collected to calculate surface water flow speeds for field validation of satellite-derived velocities (FluViSat project: Hydrological Flow Measurement from Satellite Video).
- Field validation spans multiple sites and flow conditions to support satellite-based velocimetry processing.

## Data content
- Data: one MP4 video file and one SRT file per video; Burdekin River and Uono River videos include only MP4 files.
- Resolutions: 1080P and 4K.
- Video length: 20–30 seconds per clip.
- Calibration: pre-flight calibration not required; in-processing scaling uses manual measurements of identifiable static features.
- Site coordinates (approximate) provided for each location.

## Field instrumentation
- Primary: standard unmodified DJI Air 2S consumer-grade cameras.
- Additional field tools: laser distance meters; boats-mounted Acoustic Doppler Current Profiler (ADCP) equipment (ADCP data not included in the dataset).

## Collection method
- Nadir-view videos captured by hovering over the center of the flowing water body; altitude chosen to capture full water width.

## Experimental design / sampling regime
- Sites chosen for favorable flow and surface conditions for both drone and satellite velocimetry processing.
- Video captures occurred on multiple dates per site to cover varying flow states.

## Quality control
- Drone camera settings optimized for stable, sharp, well-lit, correctly exposed footage.
- Independent observations of water width conducted to verify results from processed videos.

## Nature and units of recorded values
- Video data (MP4) and accompanying subtitles (SRT) per video.
- No pre-flight calibration; scaling performed during processing using identifiable features.

## Site locations
- Burdekin River, Australia (River) — latitude -20.628567, longitude 147.165902
- Falls Of Lora, United Kingdom (Tidal) — latitude 56.456156, longitude -5.393815
- River Tweed, United Kingdom (River) — latitude 55.722825, longitude -2.162671
- Uono River, Japan (River) — latitude 37.2458506, longitude 138.9275143
- River Rhine at Rhine Falls, Switzerland (River) — latitude 47.674231, longitude 8.609999

## Data structure
- Files organized into folders by site and date using the format X_YYYYMMDD (X = site code).
  - Burdekin River: site code Burdekin; dates = 3
  - Falls Of Lora: site code Lora; dates = 5
  - River Rhine at Rhine Falls: site code Rhine; dates = 1
  - River Tweed: site code Tweed; dates = 1
  - Uono River: site code Uono; dates = 1 (two locations ~1 km apart: Negoya Bridge ref=1 and Horinouchi ref=2)
- Each video file named: DJI_ref_X_DDMM2022 (DJI = drone type, ref = image ref, X = site name, DDMM = date).
- Datasets include multiple videos per site/date; Uono has two locations.

## Author contributions
- N. Everard: primary author and contact for the data.
- M. Randall: collected Burdekin videos and provided Uono footage; methodological expert.