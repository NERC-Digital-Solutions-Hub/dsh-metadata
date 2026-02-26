# Plot_locations_metadata.rtf

## Purpose and scope
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design and sampling regime
- Three transects, each 75 m long, laid out 20 m apart across a hillslope and running perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at locations listed in Plot_locations.csv; some locations include a second borehole.
- Boreholes labeled 'new' do not differ from those labeled 'old'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in degrees, minutes, and seconds and converted to decimal degrees.
- Coordinates also captured as six-figure Ordnance Survey National Grid references.

## Data structure and field descriptions
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections, base maps, and display notes
- Users must ensure correct projection and base map to display sample sites accurately.
- Longitude/Latitude values use GCS_WGS_1984 (WKID: 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).

## Additional notes
- An image (courtesy Welsh Government) illustrates the correct locations.