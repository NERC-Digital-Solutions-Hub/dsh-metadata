# Supporting documentation for: Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

- Purpose and context
  - Provides field validation data for surface water flow speeds measured from satellite video (FluViSat project: Hydrological Flow Measurement from Satellite Video).
  - Dataset supports comparison between drone-derived velocities and satellite-derived velocities across multiple sites and flow conditions.
  - Part of Future-EO-1 EO Science for Society; funded by the European Space Agency (ESA).

- Field sites, dates, and flow conditions
  - Burdekin River, Australia – 7–8 January; 18 May; high flow conditions.
  - River Tweed, Norham, England – 15 March; medium flows.
  - Falls of Lora, Connel, Scotland – 16–18 March; 14, 16, 17 July; tidal race at ebb with various flow conditions.
  - Uono River, Negoya, Japan – 10 May; medium–high flows.
  - Rhine Falls (Rhine River), Switzerland – 18 August; low–medium flows.
  - All fieldwork complied with national drone regulations and required permissions.

- Fieldwork instrumentation
  - Primary drone: DJI Air 2S (standard, unmodified).
  - Additional instruments for width and flow speed context: laser distance meters and boats-mounted Acoustic Doppler Current Profiler (ADCP) equipment.
  - ADCP and laser tools are not included in the provided dataset.

- Data collection methodology
  - Nadir-view videos captured with drones hovering over the center of the flowing water to cover full width.
  - Video durations: 20–30 seconds per capture.
  - Site selection aimed at favorable conditions for both drone and satellite velocimetry, with safety considerations.

- Quality control and processing notes
  - Drone camera settings optimized for stable, sharp, well-lit, properly exposed water-surface footage.
  - Independent observations of river width used to verify results from processed videos.
  - Calibration: no on-site calibration required before capture; post-processing calibration performed using manual measurements of identifiable static features in imagery.

- Data contents and structure
  - Files: One MP4 video file and one SRT file per video; Burdekin and Uono include only MP4s (no SRTs).
  - Folder organization: by site and date with format X_YYYYMMDD, where X is site code (Burdekin, Lora, Rhine, Tweed, Uono).
  - Video naming: DJI_ref_X_DDMM2022 (DJI type, reference, site code, day, month).
  - Uono River videos captured at two locations (~1 km apart): Negoya Bridge (ref=1) and Horinouchi (ref=2).
  - Site date counts: Burdekin (3 dates), Falls of Lora (5), Rhine (1), Tweed (1), Uono (1).

- Site location metadata
  - Burdekin River, Australia (River), approx. -20.628567, 147.165902
  - Falls of Lora, UK (Tidal), approx. 56.456156, -5.393815
  - River Tweed, UK (River), approx. 55.722825, -2.162671
  - Uono River, Japan (River), approx. 37.2458506, 138.9275143
  - Rhine Falls (Rhine River), Switzerland (River), approx. 47.674231, 8.609999

- Data access and custodianship
  - Primary contact: N. Everard (data originator and first point of contact).
  - M. Randall contributed videos for Burdekin and Uono and provided subject-matter expertise on the methodology.
  - Data stored and referenced within the NERC Environmental Information Data Centre (EIDC); linked to Everard & Randall (2024).

- How the data can be used
  - Support validation of satellite-derived surface water velocity measurements.
  - Enable development of data products and self-serve insights (e.g., integration with satellite data for cross-site velocity comparisons).
  - Potential to combine with in-situ measurements (laser, ADCP data) for broader hydrological analyses, noting that these auxiliary data are not included in the dataset.

- Limitations and considerations
  - Visual data require processing to derive velocities; no numerical velocity values are provided directly in the videos.
  - Some sites have only MP4s (no subtitle data); dataset value relies on post-processing for speed extraction and calibration.
  - Spatial precision relies on manual calibration using identifiable static features in imagery.

- Suggested citations
  - For dataset attribution and methodology, reference Everard & Randall (2024) and the associated NERC EIDC record.