# Metadata for 6_Ivankov_background_radiation.csv

## Overview
- Contains spatial and measurement metadata for background radiation sampling sites.
- Key spatial fields: latitude and longitude in decimal degrees using WGS-84.
- Measurements include ambient dose rates at two heights (0.1 m and 1 m) and a site descriptor of habitat type.
- Notes indicate some sites were inaccessible, but locations remain documented for completeness.

## Data schema and field descriptions
- latitude
  - Description: Location of sampling site
  - Data format: Decimal degrees
  - Coordinate reference system: WGS-84
  - Accuracy: Approximately 10 m or less
  - Notes: Collected with GPS receiver (Garmin GPSmap 78S)

- longitude
  - Description: Location of sampling site
  - Data format: Decimal degrees
  - Coordinate reference system: WGS-84
  - Accuracy: Approximately 10 m or less
  - Notes: Collected with GPS receiver (Garmin GPSmap 78S)

- Analysis_type_1_or_2
  - Description: Indicates site purpose
  - Value meanings: 1 = dose measurement and soil sampling; 2 = only dose measured
  - Units: n/a
  - Notes: n/a

- at_0.1m
  - Description: Ambient dose rate at height 0.1 m above ground
  - Data format: n/a
  - Units/Methodology: Certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine)
  - Notes: n/a

- at_1m
  - Description: Ambient dose rate at height 1 m above ground
  - Data format: n/a
  - Units/Methodology: Certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine)
  - Notes: n/a

- Sampling_site_descriptio n
  - Description: Habitat type at sampling site
  - Units/Methodology: n/a
  - Notes: Seven sites were inaccessible; locations are retained for completeness

> Observed metadata issue: field name "Sampling_site_descriptio n" contains an unintended space, indicating potential data quality/standardization problems.

## Data quality and limitations
- Spatial accuracy is around 10 meters or less based on the cited GPS source.
- Some sites were inaccessible, though their coordinates remain to preserve completeness.
- Field names contain typographical inconsistencies (e.g., "Sampling_site_descriptio n"), which may affect data handling and standardization.
- Data relies on specific dosimetry equipment (RKS-01), with no explicit calibration details provided in this metadata excerpt.

## GIS considerations and recommendations
- Ensure coordinate data are interpreted as WGS-84 decimal degrees for mapping and analysis.
- Consider cleaning field names to standard formats (e.g., Sampling_site_description) to improve interoperability.
- When building map-based products:
  - Create layers for site locations (points) using latitude/longitude.
  - Attach attributes for analysis type, dose rates at 0.1 m and 1 m, and habitat description.
  - Include metadata notes on accessibility and data source (GPS device and dosimetry equipment).
- Validate and possibly harmonize units/methodology if combining with other radiation datasets or GIS layers.
- If combining with other datasets, use a common site identifier or create a robust join key from available fields.

## Potential uses for GIS specialists
- Visualizing spatial distribution of background radiation across sampling sites.
- Comparing dose rates at different vertical heights as a 3D-enabled visualization.
- Linking habitat-type information to radiation measurements for ecological risk assessments.
- Documenting data provenance and accessibility limitations within map pop-ups and metadata layers.

## Notes on provenance and usage
- Metadata points to specific instrument types and measurement heights, which should inform interpretation of dose values.
- Accessibility note indicates the dataset favors completeness in spatial coverage even when field collection was not possible at some sites.