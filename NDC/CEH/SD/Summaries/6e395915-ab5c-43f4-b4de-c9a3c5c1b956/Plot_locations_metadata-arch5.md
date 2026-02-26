# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which contains the locations of sampling sites used in a hillslope sampling design.

## Experimental design / Sampling regime
- Three transects, each 75 meters long and 20 meters apart, across a hillslope perpendicular to the River Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have an additional borehole labeled 'new' (these are not functionally different from 'old').

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded as degrees, minutes, seconds, then converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Data structure details
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections / units and display guidance
- For longitude and latitude: GCS_WGS_1984 (WKID: 4326, EPSG).
- For Eastings and Northings: OSGB1936 British National Grid (WKID: 27700, EPSG).
- Ensure the base map and data are in the correct projection to display sample sites accurately.
- An image (courtesy Welsh Government) indicates correct locations.

## Data quality and governance considerations for Data Stewards
- Maintain consistency between coordinate representations (lat/long vs OS grid).
- Verify the 8-column data structure and field descriptions in Plot_locations.csv.
- Confirm that the projection settings are correctly applied in GIS workflows to avoid mislocation.
- Preserve metadata about measurement date/time (UTC/GMT) for temporal alignment.
- Ensure provenance and accuracy notes are kept up to date, including any guidance linked to the 8-column schema.

## Practical notes for use and sharing
- Users should validate the coordinate system when loading data into mapping tools.
- The document provides clear guidance on which projection to use for each coordinate type to maintain interoperability.
- The embedded reference to an illustrative image helps users verify correct site placements.