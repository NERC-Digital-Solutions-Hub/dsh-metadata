# Plot_locations_metadata.rtf

## Overview
- Metadata accompanying Plot_locations.csv, which contains sampling site locations.
- Context: three 75 m transects 20 m apart across a hillslope perpendicular to the river Hiraethlyn; boreholes installed to bedrock along transects, with some locations labelled as 'new' (not differing from 'old').

## Experimental Design
- Transects: three, each 75 meters long, spaced 20 meters apart.
- Sampling layout: boreholes installed to bedrock at indicated locations in Plot_locations.csv; some locations have a second borehole.
- Labels: boreholes marked as 'new' but do not differ from 'old'.

## Collection Methods
- Coordinates collected with a handheld Garmin GPS device.
- Latitude and Longitude originally in degrees, minutes, seconds (DMS) and converted to decimal degrees.
- Also collected as six-figure Ordnance Survey National Grid references.

## Nature and Units of Recorded Values
- Latitude and Longitude recorded in decimal degrees (converted from DMS).
- OS Grid references recorded as six-figure coordinates.

## Details of Data Structure
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate Reference Systems and Projections
- Longitude/Latitude values: GCS_WGS_1984 (EPSG 4326)
- Eastings/Northings: OSGB1936 British National Grid (EPSG 27700)
- Elevation: metres above Ordnance Datum Newlyn (ODN)
- Important note: Users must ensure the correct projection is used and that the base map matches the projection to display sample sites accurately.

## Practical Notes
- The associated image (courtesy Welsh Government) illustrates correct locations (not included in this text).
- Ensure that plotting tools use the specified CRS to avoid misrepresentation of site locations.