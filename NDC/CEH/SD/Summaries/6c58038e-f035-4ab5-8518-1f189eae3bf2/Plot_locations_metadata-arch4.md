# Plot_locations_metadata.rtf

## Experimental design and Sampling regime
- Three transects, each 75 m long and 20 m apart, identified across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at locations specified in Plot_locations.csv.
- Some locations include a second borehole; boreholes labeled 'new' do not differ from those labeled 'old'.

## Collection Methods and instrumentation
- Co-ordinates collected with a handheld Garmin GPS device.

## Nature and Units of recorded values
- Latitude and Longitude recorded in degrees, minutes, seconds, then converted to decimal degrees.
- Co-ordinates also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv provides the locations of sampling sites.
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate reference systems and display considerations
- Ensure the correct projection is used and the base map is in the correct projection to display sample sites accurately.
- Longitude/Latitude values use GCS_WGS_1984 WKID: 4326 (EPSG).
- Eastings/Northings use OSGB1936 British National Grid WKID: 27700 (EPSG).

## Additional notes
- An image (courtesy of Welsh Government) illustrates the correct locations.