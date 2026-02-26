# Plot_locations_metadata.rtf

- This document contains metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design / Sampling regime
- Three transects, each 75 meters long and 20 meters apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; at some locations a second borehole was drilled.
- Boreholes labeled 'new' do not differ from 'old' boreholes.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references (OSGB).

## Details of data structure
- Plot_locations.csv provides locations of sampling sites.
- 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and display guidance
- Ensure correct projection for base maps to display sites accurately.
- Longitude/Latitude use GCS_WGS_1984 (WKID 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID 27700, EPSG).

## Notes
- An image (courtesy Welsh Government) illustrates correct site locations.