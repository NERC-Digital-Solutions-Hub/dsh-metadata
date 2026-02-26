# Plot_locations_metadata.rtf

## Purpose and contents
- Metadata for Plot_locations.csv, which holds the locations of the sampling sites.

## Experimental design and sampling regime
- Three 75 m long transects, 20 m apart, identified across a hillslope and running perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at locations specified in Plot_locations.csv.
- At some locations a second borehole was drilled; these are labeled 'new' and do not differ from boreholes labeled 'old'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in decimal degrees (converted from degrees, minutes, seconds).
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Data structure and columns
- Plot_locations.csv provides locations of sampling sites.
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projection and mapping notes
- Ensure the correct projection is used and the base map is in the correct projection to display sample sites accurately.
- For longitude/latitude: GCS_WGS_1984 WKID: 4326 (EPSG)
- For Eastings/Northings: OSGB1936 British National Grid WKID: 27700 (EPSG)

## Visual reference
- An image (Courtesy Welsh Government) illustrates the correct site locations.