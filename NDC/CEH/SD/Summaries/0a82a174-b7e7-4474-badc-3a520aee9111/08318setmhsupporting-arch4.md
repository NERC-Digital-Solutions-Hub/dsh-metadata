# Supporting Documentation for Dataset: UK Saltmarsh Monitoring Project

## Overview
- A dataset detailing sediment elevation and environmental metadata from UK saltmarsh sites, collected using standardized SET-MH methods.
- Projected for ongoing data quality checks, analysis, and integration with broader data communities.

## Dataset composition
- Four CSV files comprising the dataset:
  - 08318setmhsitemetadata.csv: site-related metadata
  - 08318setmhsamplingmetadata.csv: sampling-related metadata
  - 08318setdata.csv: sediment elevation measurements
  - 08318mhdata.csv: marker horizon measurements
- Each file uses a consistent unique ID framework to link plots, metadata, photos, and sites.

## Study scope and locations
- Data collected along the UK coastline across 16 saltmarsh marshes (UKCEH sites) from Dornoch Firth to Solent.
- Included sites:
  - Dornoch Point, Crook of Baldoon, Caerlaverock, Campfield Marsh
  - Warton Marsh, Banks Marsh, Marshside
  - Stiffkey, Brancaster Beach, Blakeney
  - Wolferton Marsh, Bulldog Sands East, Bulldog Sands West
  - West Itchenor, Pilsey/Thorney Island, Gutner Point
- Exact plot locations recorded with GPS; elevations also sourced from LIDAR (year recorded) and GNSS measurements.

## Data collection timeline
- Initial measurements in spring/summer 2023; follow-up monitoring in spring and autumn 2024.
- Annual monitoring planned (monotiring in spring; autumn when possible).

## Methods and instrumentation
- Primary method: Surface Elevation Table - Marker Horizon (SET-MH).
- Installation methodology (standardized, three SET plots per marsh at similar elevation and mid-marsh plant communities):
  - SET bases installed with four collar orientations (N, E, S, W) relative to a central 50 x 50 cm quadrat.
  - Feldspar clay applied to quadrats to trace sediment elevation changes.
  - Replication across sites to capture variability; nine pins per SET or core-based measurements for horizons.
  - Elevation estimated from GNSS; LIDAR-based elevations used for baseline context.
  - Temporary platforms used during installation to minimize disturbance.
- Instruments and calibration:
  - dGPS, sediment corers, digital levels; petrol-driven postdriver for SET installation.
  - Instruments calibrated per manufacturer specs.
- Data processing:
  - Analysis planned in R; scripts to be shared with publications.
  - LIDAR-derived elevations calculated in QGIS using a 20 m diameter circle around each plot; year of lidar data recorded.

## Variables and data structure
- Data collected include:
  - Elevation measurements (mm) from SETs; depth to horizons for marker horizons
  - Metadata: site coordinates (latitude/longitude), depth of rSET, GNSS elevation, LIDAR elevation and year, plant community composition (DAFOR, NVC codes), sediment observations, site and weather conditions
  - Orientation and replicate details for readings (e.g., pins 1-9; quadrants; SET location codes)
- Species and vegetation data:
  - Dominant, abundant, frequent, occasional, rare species by codes (e.g., Ap = Atriplex prostrata; Pm = Puccinellia maritima; Se = Salicornia europaea; Spartina sp.; etc.)
  - NVC saltmarsh communities included (e.g., SM13a, SM13c, SM14a, SM14c, SM16a) with sub-communities
- Data file structures:
  - 08318setmhsitemetadata.csv: location codes, coordinates, depth, lidar year, LIDAR elevation, GNSS elevation, community codes, methods
  - 08318setmhsamplingmetadata.csv: row order, sampling timestamps, plot IDs, photos, species codes by cover category, NVC, weather and site notes, installation notes
  - 08318setdata.csv: row order, location code, plot code, replicate code, timestamps, orientation, pin readings (height in mm), notes
  - 08318mhdata.csv: row order, location code, plot code, replicate, timestamps, horizon depth, notes

## Data quality and governance
- Quality control:
  - Regular photographs of plots; metadata and data reformatted and linked by unique IDs
  - Calibration per manufacturer specs; data described with units and clear field descriptions
- Data accessibility and future use:
  - Data intended for use in future publications and broader data communities
  - Linkages between plots, metadata, photos, and sites facilitated by unique IDs

## Appendices and references
- Appendix 1: NVC Saltmarsh community floristic tables (e.g., SM13a, SM13c, SM14a, SM14c, SM16a)
- Appendix 2: Locations of all SET bases with detailed coordinates and plot associations
- Reference: Lynch, J. C., Hensel, P., & Cahoon, D. R. (2015). SET-MH protocol for monitoring wetland elevation dynamics

## Contacts
- Enquiries: enquiries@ceh.ac.uk
- UKCEH locations: Bangor, Edinburgh, Lancaster, Wallingford (headquarters)