# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

- Overview
  - Dataset of sediment elevation measurements using Surface Elevation Tables and Marker Horizons (SET-MH) plus environmental metadata.
  - Coverage: UK saltmarsh sites across multiple estuary systems from Dornoch Point to the Solent, including 16 marshes and numerous SET bases.
  - Temporal scope: initial measurements in spring/summer 2023; follow-up in spring and autumn 2024; annual monitoring planned.

- Data collection and installation
  - Installation methodology: UKCEH rSET bases and marker horizons installed following Lynch et al. (2015); three SET plots per marsh at mid-marsh, ~5 m from creek edge.
  - Plot layout and replication: four positions 1.5 m N, E, S, W around each SET; nine pins per measurement from outside inwards; marker horizons measured in triplicate across plots.
  - Marker preparation: potassium feldspar clay applied within a 50 x 50 cm quadrat to ensure a consistent horizon.
  - Controls and reference data: plots selected for consistent elevation and plant community representation; vegetation classified and monitored (DAFOR/NVC); elevation estimated from LIDAR; exact plot locations captured with GPS; temporary platforms used to minimize disturbance.

- Data collection specifics
  - Elevation data: recorded in millimeters from rSET plots across multiple orientations (1-8) and quadrants (N, E, S, W); depth to marker horizons measured with cores.
  - Metadata: latitude, longitude, depth of rSET, LIDAR elevation (with year), GNSS elevation, vegetation codes (DAFOR/NVC), sediment observations, site features, weather conditions.
  - Periodicity: annual measurements in spring, with potential autumn monitoring when feasible.
  - Sample size: 48 SETs across 16 marshes, totaling 4,104 elevation observations.

- Instruments, calibration and data handling
  - Instruments: dGPS, sediment corers, digital levels, and a petrol-driven postdriver for installation.
  - Calibration: instruments calibrated per manufacturer specifications.
  - Units and data types: elevations and horizon depths in millimeters; descriptive metadata and occupational notes in text fields.
  - Analysis: planned processing in R; LIDAR-based elevation estimates calculated in QGIS; data quality controlled with photographs and linked metadata.

- Data structure and contents
  - Four CSV files comprising the dataset:
    - 08318setmhsitemetadata.csv: site-related metadata (locations, coordinates, depth, lidar year, GNSS elevation, vegetation codes, NVC, observational metadata).
    - 08318setmhsamplingmetadata.csv: sampling metadata (row order, metadata codes, timestamps, plot IDs, photos, dominant/abundant/frequent/occasional/rare species codes, NVC, weather, sediment, site, installation notes).
    - 08318setdata.csv: sediment elevation measurements (location, plot, replicate, timestamps, orientation, height data).
    - 08318mhdata.csv: marker horizon measurements (similar structure to setdata.csv).
  - Location and plotting codes: location_code (e.g., RBMS, NNBB, CHGI), plot_code (SETnumber_LocationCode), replicate_code (pin/core), timestamp_TN, orientation, height_pin_mm, notes.
  - Appendix data:
    - Appendix 1: NVC saltmarsh communities (e.g., SM13a, SM14a, etc.).
    - Appendix 2: Locations and coordinates of all SET bases with site-specific identifiers.

- Geospatial and site context
  - Sites include: Dornoch Point, Crook of Baldoon, Caerlaverock, Campfield Marsh, Warton Marsh, Banks Marsh, Marshside, Stiffkey, Brancaster Beach, Blakeney, Bulldog Sands East/West, West Itchenor, Pilsey, Gutner Point, among others.
  - Each SET base is linked to site metadata, with coordinates and associated marsh/estuary information.

- References and appendices
  - Primary methodological reference: Lynch, Hensel, Cahoon (2015) on the SET-MH protocol for wetland elevation monitoring.
  - Appendices provide floristic context (NVC communities) and exact SET base locations and coordinates.

- Practical implications for analysts
  - Provides standardized, QA’d time-series of saltmarsh elevation across multiple sites suitable for assessing elevation dynamics, sea-level rise responses, and environmental health performance.
  - Enables cross-site comparisons and integration with additional data streams (LIDAR, vegetation classifications, weather).
  - Datasets are designed for integration into monitoring portals and for reuse in published analyses, with planned R-based processing scripts.

- Access and contact
  - Contact: enquir ies@ceh.ac.uk
  - UK Centre for Ecology & Hydrology offices listed for further information and data access.