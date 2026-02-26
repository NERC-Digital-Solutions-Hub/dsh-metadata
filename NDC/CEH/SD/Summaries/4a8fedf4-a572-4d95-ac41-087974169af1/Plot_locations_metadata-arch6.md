# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which contains the locations of sampling sites.

## Experimental design
- Three transects, each 75 m long and 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock; some locations have a second borehole labeled 'new' (these are not different from 'old').

## Collection methods and instrumentation
- Co-ordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude originally recorded in degrees, minutes, seconds and converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Data structure (Plot_locations.csv)
- Columns (8 total):
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projections
- For longitude/latitude: GCS_WGS_1984 (WKID 4326, EPSG)
- For Easting/Northing: OSGB1936 British National Grid (WKID 27700, EPSG)
- Users must ensure the correct projection is used and that the base map is in the correct projection to display sample sites accurately.

## Usage notes
- An image (Courtesy Welsh Government) illustrates the correct locations (reference only).
- When combining with other data, ensure consistent projection and units; be mindful of the GMT time reference for Time field.