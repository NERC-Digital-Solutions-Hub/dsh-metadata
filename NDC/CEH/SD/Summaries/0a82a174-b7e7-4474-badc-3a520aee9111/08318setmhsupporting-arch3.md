# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

- A dataset documenting sediment elevation dynamics and environmental metadata across UK saltmarsh sites using Surface Elevation Tables and Marker Horizons (SET-MH).
- Includes field installation methods, data collection protocols, data structure, QA processes, and mapping of sites and vegetation communities.

## What has been recorded

- Sediment elevation measurements from rSET plots using SET-MH method.
- Environmental metadata: soil composition observations, plant cover, depth of the rSET, and installation details.
- All data are linked to unique plot identifiers and site metadata for traceability.

## Where and when data were collected

- Locations: 16 saltmarsh sites across the UK, spanning Dornoch Point, Crook of Baldoon, Caerlaverock, Campfield Marsh, Warton Marsh, Banks Marsh, Marshside, Stiffkey, Brancaster, Blakeney, Bulldog Sands East/West, West Itchenor, Pilsey/Thorney Island, Gutner Point, and others in Solent/Wash/N Norfolk regions.
- Temporal coverage: initial measurements Spring/Summer 2023; follow-up in Spring and Autumn 2024; annual monitoring planned in Spring when possible.

## How data were collected

- Standard SET-MH methodology installed per Lynch et al. (2015) protocol.
- Installation: three SET plots per marsh with similar elevation and mid-marsh plant communities; plots positioned at least 5 m from creek edge.
- Marker horizons prepared using potassium feldspar clay within quadrats surrounding SET sites; replication across sites to capture variability.
- Elevation derived from GNSS measurements; elevation estimates also derived from LIDAR data (with year noted).
- Plant community data recorded using DAFOR scale and National Vegetation Classification (NVC) codes.
- Weather and site observations captured as metadata.

## Experimental design and replication

- Replication: measurements across multiple saltmarsh sites with nine pins per SET from various orientations (initially eight; later nine).
- Controls: three SET plots per marsh at similar elevation and representative mid-marsh plant community (e.g., SM13–SM14 families); plots spaced to minimize disturbance.
- Calibration and consistency: same installation method across plots; instruments calibrated per manufacturer specs; temporary platforms used to reduce disturbance during installation/monitoring.

## Data collection specifics

- Elevation data: mm measurements from rSET plots in collar orientations (1–8) or quadrants (N, E, S, W); measurement from outside inward using pins (1–9 for rSET; 1–3 for horizons).
- Horizons: depth of feldspar horizons measured with corer and ruler (three measurements per core; averaged to 1 mm precision).
- Metadata: latitude, longitude, rSET depth, GNSS elevation, LIDAR elevation (and year), vegetation composition (DAFOR/NVC), sediment and site/weather observations.
- Periodicity: annual spring measurements; optional autumn monitoring.

## Data structure and contents

- Four CSV files comprising the dataset:
  - 08318setmhsitemetadata.csv: site-related metadata (locations, SET IDs, GPS coordinates, rSET depth, LIDAR year/elevation, etc.).
  - 08318setmhsamplingmetadata.csv: sampling-related metadata (row order, metadata codes, timestamps, plot IDs, dominant/abundant/frequent/occasional/rare species, NVC codes, notes).
  - 08318setdata.csv: sediment elevation measurements (location, plot, replicate, timestamp, orientation, height pin, notes).
  - 08318mhdata.csv: marker horizon measurements (as above with horizon-specific fields like depth_to_horizon_m and notes).
- Variables include:
  - Location_code, SET_ID, Latitude, Longitude, Depth_rSET, timestamp_lidar, LIDAR_elevation, Elevation_m, GCS_notes, Instrument.
  - plot_code (SETnumber_LocationCode), replicate_code, timestamp_T0/TN, orientation, height_pin_mm, notes.
  - For vegetation: dominant, abundant, frequent, occasional, rare, NVC, etc.
- Units: elevations in millimetres, depths in millimetres, coordinates in decimal degrees; other measurements follow described field formats.

## Data processing and analysis

- Planned processing and analysis in R; an accompanying R script is intended to be included with future publications.
- Quality control procedures include photography of each plot and cross-checking metadata with unique IDs to ensure traceability.

## Data governance and openness

- The dataset uses unique ID codes to link site, metadata, photos, and data.
- Metadata are comprehensive to support verification and reuse; data are prepared to support clear interpretation and future analyses.
- Data management and openness considerations are addressed through consistent metadata and standardized data structures; explicit public sharing arrangements are described as potential barriers in monitoring-framework contexts, but this dataset provides a framework for traceability and reproducibility.

## References

- Lynch, J. C., Hensel, P., & Cahoon, D. R. (2015). The surface elevation table and marker horizon technique: A protocol for monitoring wetland elevation dynamics. Natural Resource Report NPS/NCBN/NRR.

## Appendices highlights

- Appendix 1: NVC Saltmarsh plant communities included (e.g., SM13a, SM13c, SM13d, SM14a, SM14c, SM16a) with associated sub-communities.
- Appendix 2: Locations and coordinates of all SET bases (example entries: RBMS1–RBMS3 at Marsh Side, Warton Marsh; RBBS1–RBBS3 at Bank Side; SWCF1–SWCF3 at Campfield Marsh; DFDP entries at Dornoch Point; CHWI/CHPS/CHGP entries for Chichester/ Pilsey/Gutner Point; and others across the UK).