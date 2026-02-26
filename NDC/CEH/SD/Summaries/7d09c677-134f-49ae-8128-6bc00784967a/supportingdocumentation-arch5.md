# Brief Overview

- Purpose: Repeat electrical resistivity tomography (ERT) measurements to monitor soil resistivity changes across four sites throughout the agricultural growing season, capturing transitions from construction to production to post-harvest stages (Spring, Summer, Autumn; 2021).
- Survey cadence: Initial measurements (April/May 2021), Summer measurements (June/July 2021), and final measurements (September 2021).
- Positioning accuracy: Survey transects geolocated with a Leica GNSS system with ~0.01 m accuracy to ensure repeatability.

## Data Collection and Methodology

- Each survey location used a single 19 m ERT transect with 96 electrodes spaced 20 cm apart (Campus Tigre system).
- Configuration: Wenner Array to obtain subsurface resistivity with sufficient vertical and horizontal resolution.
- Readings: Approximately 660 apparent resistivity measurements per traverse, down to about 1 m below ground level.
- Field tools: Data collected with ImagerPro2006; processing performed with Geotomo's Res2DInv.

## Sites and Survey Details

- Study supported by the LANDWISE NFM research project.
- Survey locations (start and end coordinates recorded for each transect):
  - Lower Hampen Farm – Barn Ground
  - Lower Hampen Farm – Flat Ground
  - Manor Farm – Whittington Hill
  - Hendred Farm – Lockinge (Untraffic) and East Hendred (Traffic A/B)
- Detailed coordinates provided for reproducibility and site-level tracking.

## Data Structure, Units, and Documentation

- Data format: Res2DInv format (BarnGround_April.dat used as an example).
- Key data characteristics:
  - 0.2 m electrode spacing
  - Wenner Array indicated
  - ~660 data points per survey
  - Data points: x-location, electrode spacing, and apparent resistivity values
  - Data stored as Apparent Resistivity (Ohm.m); no IP data indicated
- Additional context: Documentation includes field structure notes and an explicit example of the data file layout.

## Quality Control and Data Processing

- Pre-survey quality checks: Software ensures good electrode-ground contact; misbehaving electrodes are re-established.
- Post-collection processing: Removal of noisy data points before inversion in Res2DInv to improve data quality and reliability.

## Governance, Reuse, and Provenance

- Project provenance: LANDWISE NFM research project; dataset tied to specific field campaigns and site locations.
- Reusability: Detailed description of measurement setup, data structure, and processing workflow (Res2DInv format and parameters) supports data reuse and reproducibility.
- References for data format: Res2DInv documentation available from Geosoftware Geotomo (URL provided in the data notes).