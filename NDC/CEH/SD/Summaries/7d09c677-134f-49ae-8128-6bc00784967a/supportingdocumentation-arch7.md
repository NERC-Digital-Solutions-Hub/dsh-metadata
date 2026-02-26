# Brief Overview

- Objective: Repeat electrical resistivity tomography (ERT) measurements to capture how soil resistivity changes across four sites throughout the agricultural growing season, to distinguish between construction, production, and post-harvest stages.
- Temporal coverage: Measurements taken in Spring, Summer, and Autumn 2021 (April/May, June/July, September).
- Survey precision: Each transect positioned with a Leica GNSS system (~0.01 m accuracy) for repeatable locations.

- Field setup and geometry:
  - Each site uses a single 19 m ERT transect with 96 electrodes spaced every 20 cm.
  - Equipment: Campus Tigre system; Wenner Array configuration.
  - Depth/resolution: Data collected down to ~1 m below ground level (bgl); approximately 660 apparent resistivity readings per transect.

- Data collection and processing tools:
  - Field data collection: ImagerPro2006.
  - Data processing: Geotomo Res2DInv.

- Project context:
  - Data collected to support the LANDWISE NFM (Land Management in Lowland Catchments for Integrated Flood Risk Reduction) research project.
  - Site locations include Lower Hampen Farm (Barn Ground and Flat Ground), Manor Farm (Whittington Hill), Hendred Farm (Lockinge and East Hendred), with start/end coordinates provided for each transect.

- Method details:
  - Resistivity measurement principle: Wenner Array, with current between outer C1 and C2 electrodes and potential difference measured at inner P1 and P2 electrodes; deeper investigations achieved by increasing electrode spacing (a).
  - Measured parameter: Apparent Resistivity (Ohm.m).

- Quality control and data integrity:
  - Pre-survey checks for electrode-ground contact; re-establishment of poor contacts.
  - Post-survey data screening in Res2DInv to remove noisy points before inversion.

- Data structure and availability:
  - Data stored in Res2DInv format (example: BarnGround_April.dat).
  - File metadata includes electrode spacing (0.2 m), array type (Wenner), data point count (660), and point-by-point resistivity values.
  - Reference for data structure and download: Geotomo Res2DInv resources (link provided in the document).