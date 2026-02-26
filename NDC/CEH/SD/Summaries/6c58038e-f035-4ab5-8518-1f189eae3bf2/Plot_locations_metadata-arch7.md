# Plot_locations_metadata.rtf

## Purpose
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design
- Three transects, each 75 m long and 20 m apart, identified across a hillslope and running perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled as 'new' (these do not differ from 'old').

## Collection methods
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded as degrees, minutes, seconds and converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv contains locations of sampling sites and consists of 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections/Coordinate reference
- For longitude and latitude: GCS_WGS_1984 (WKID: 4326, EPSG)
- For Easting and Northing: OSGB1936 British National Grid (WKID: 27700, EPSG)
- Users must ensure the correct projection is used and that the base map is in the correct projection to display sample sites accurately.

## Additional notes
- An image (Courtesy Welsh Government) is provided to illustrate the correct locations.