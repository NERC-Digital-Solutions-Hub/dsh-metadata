# Plot_locations_metadata.rtf

## Summary
- Metadata describes Plot_locations.csv, which holds the locations of sampling sites.
- Experimental design includes three 75 m transects (20 m apart) across a hillslope, perpendicular to the river Hiraethlyn; each transect has four boreholes drilled to bedrock, with some locations having a second borehole labeled 'new' that is not different from 'old'.
- Coordinates were collected with a handheld Garmin GPS.

## Experimental design
- Three transects, each 75 meters long.
- Transects are 20 meters apart.
- Transects run across a hillslope, perpendicular to the river Hiraethlyn.
- Along each transect: four boreholes drilled to bedrock.
- Some sites have a second borehole labeled 'new'; these are not distinguished from 'old'.

## Collection methods and instrumentation
- Coordinates collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in degrees, minutes, seconds, then converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv provides locations of sampling sites.
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projection notes
- Longitude and latitude values use GCS_WGS_1984 (WKID: 4326, EPSG).
- Eastings and Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).
- Users must ensure the correct projection is used and that the base map is in the correct projection to display sample sites accurately.

## Additional notes
- An image (Courtesy Welsh Government) is referenced as illustrating correct locations.