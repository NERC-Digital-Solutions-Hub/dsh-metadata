# Elter_light_2018-2019.txt

## Overview
- Weekly to monthly vertical profiles of underwater photosynthetically active radiation (PAR) taken between May 2018 and December 2019.
- Location: deepest point of Elterwater inner basin (Lat 54.4287, Lon -3.0350).
- Instrument: LI-COR LI-192 underwater quantum sensor.

## Spatial and Temporal Coverage
- Single geographic point for mapping and visualization.
- Temporal span: May 2018 – December 2019.
- Sampling frequency: weekly to monthly, varying over the period.

## Data Collection Methods
- PAR measured at depths from 0.5 to 6.0 meters, in 0.5 m increments.
- Measurements verified through visual inspection.

## Data Structure
- Columns: Date (YYYY-MM-DD), Depth (m), Light (μmol s^-1 m^-2).

## Quality and Processing Notes
- Measurements checked via visual inspection (basic quality check).

## GIS-Relevant Use and Considerations
- Suitable for creating vertical PAR profiles at a fixed location; can be incorporated into GIS as:
  - 3D representations (depth as z, Light as attribute) or time-enabled profiles.
  - Spatial datasets augmented with bathymetry for contextual mapping.
- Considerations:
  - Single-site data limits broader spatial analyses.
  - Variable sampling frequency (weekly to monthly) may require resampling or interpolation for uniform time-series visualization.
  - Ensure unit consistency (μmol s^-1 m^-2) when integrating with other datasets.