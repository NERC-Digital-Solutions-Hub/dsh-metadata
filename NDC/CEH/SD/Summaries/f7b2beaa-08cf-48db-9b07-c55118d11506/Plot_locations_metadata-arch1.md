# Plot_locations_metadata.rtf

## Overview
- Metadata accompanying Plot_locations.csv, which stores the locations of sampling sites.

## Experimental design
- Three transects, each 75 m long and 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock at indicated locations; some locations have a second borehole labeled 'new' (not different from 'old').

## Collection methods
- Coordinates collected with a handheld Garmin GPS device.
- Latitude/Longitude recorded in degrees, minutes, seconds and converted to decimal degrees; also captured as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv consists of 8 columns:
  - Name (site identifier)
  - Latitude (decimal degrees)
  - Longitude (decimal degrees)
  - Date (date of measurement)
  - Time (GMT)
  - Easting (British National Grid)
  - Northing (British National Grid)
  - ODN (elevation in metres above Ordnance Datum Newlyn)

## Coordinate reference and projections
- Longitude/Latitude values use GCS_WGS_1984 (WKID: 4326), EPSG.
- Eastings/Northings use OSGB1936 British National Grid (WKID: 27700), EPSG.
- Users must ensure the correct projection is used for base maps to display sample sites accurately.

## Data quality and units
- Elevation provided as ODN in metres.
- Date/time stamps present; time recorded in Greenwich Mean Time.

## Notes
- An accompanying image (courtesy Welsh Government) illustrates correct locations.
- New boreholes are labeled but not distinguished from old boreholes in data.