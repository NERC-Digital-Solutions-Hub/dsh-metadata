# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.
- Experimental design: three 75 m long transects, 20 m apart across a hillslope, running perpendicular to the River Hiraethlyn; along each transect four boreholes installed to bedrock, with some locations having a second borehole labeled 'new' (not different from 'old').

## Collection Methods and Instrumentation
- Coordinates collected with a handheld Garmin GPS device.
- Latitude and longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
- Also recorded as six-figure Ordnance Survey National Grid references.

## Nature and Units of Recorded Values
- Latitude and Longitude: decimal degrees (WGS 84).
- Easting and Northing: British National Grid coordinates (OSGB1936).

## Data Structure
- Plot_locations.csv consists of 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and Compatibility
- Users must ensure correct projection is used and the base map is in the correct projection to display sites accurately.
- For longitude/latitude: GCS_WGS_1984 (WKID 4326, EPSG)
- For Eastings/Northings: OSGB1936 British National Grid (WKID 27700, EPSG)

## Additional Notes
- An image (courtesy Welsh Government) illustrates the correct site locations.