# Supporting documentation for:
Drone footage of the water surface of four rivers and one tidal site in a range of flow conditions in the UK, Australia, Switzerland and Japan, 2022

- Purpose and scope
  - Provides drone video data to calculate surface water flow speeds (velocity) for field validation of flows derived from satellite video (FluViSat project).
  - Sites and conditions cover a diverse set of rivers and a tidal site under varying flow conditions, including high, medium, and low flows and tidal ebbs.
  - Funded by the European Space Agency under Future-EO-1 EO Science for Society.

- Field sites and conditions
  - Burdekin River, Australia – high flow (7–8 January; 18 May)
  - River Tweed, Norham, England – medium flows (15 March)
  - Falls of Lora, Connel, Scotland – tidal race; multiple dates during ebb with various flow conditions (16–18 March; 14, 16, 17 July)
  - Uono River, Negoya, Japan – medium-high flows (10 May)
  - Rhine Falls, Switzerland – low to medium flows (18 August)

- Data collection and instrumentation
  - Equipment: standard unmodified DJI Air 2S drones for nadir-view video; supplementary field instruments include laser distance meters and boats-mounted Acoustic Doppler Current Profiler (ADCP) data (not included in dataset).
  - Collection method: videos hovered over the center of the flowing water to capture the full width; footage is 20–30 seconds per site/date.
  - Compliance: all drone operations conducted under country-specific regulations and permissions.

- Data format and structure
  - Each video consists of one MP4 file and one SRT file (except Burdekin and Uono, which include only MP4).
  - Folder structure: organized by site and date using the format X_YYYYMMDD (X = site code).
    - Burdekin (Burdekin) – 3 dates
    - Falls Of Lora (Lora) – 5 dates
    - Rhine (Rhine) – 1 date
    - Tweed (Tweed) – 1 date
    - Uono (Uono) – 1 date, with two test locations: Negoya Bridge (ref=1) and Horinouchi (ref=2)
  - File naming: DJI_ref_X_DDMM2022 (drone type, image ref, site code, date)
  - Site coordinates (approximate): Burdekin River (-20.628567, 147.165902); Falls Of Lora (56.456156, -5.393815); River Tweed (55.722825, -2.162671); Uono River (37.2458506, 138.9275143); Rhine Falls (47.674231, 8.609999)

- Data processing and calibration
  - Calibration (scaling) performed during processing using manual measurements of distances between identifiable static features in the imagery.
  - No pre-flight calibration required beyond standard camera/gimbal checks.
  - Data used for computing surface flow speeds; ADCP and laser measurements used in the field are not included in the dataset.

- Quality control and verification
  - Drone camera settings optimized for stable, in-focus, well-lit, properly exposed footage.
  - Independent observations of river width conducted to verify video-derived results.

- Data context and usage
  - Primary aim: validate satellite-derived flow velocities (fluviometry) with ground-truth video measurements.
  - Outputs suitable for standardised reporting and integration into environmental monitoring dashboards and portals.

- Author contributions
  - N. Everard: primary author and data contact.
  - M. Randall: video collection for Burdekin and Uono; expert on methodology.

- Notes for analysts
  - Data include video-based velocity validation data; reflect a standardized approach across multiple countries and site types.
  - External field data (ADCP, laser measurements) exist but are not included in this dataset.
  - Data are part of a broader data centre (NERC Environmental Information Data Centre) and align with data stewardship practices for reuse and portal deposition.