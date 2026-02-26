# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design / Sampling regime
- Three transects, each 75 m long, 20 m apart, across a hillslope and perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled 'new' (these are not different from the 'old' boreholes).

## Collection methods and instrumentation
- Co-ordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
- Co-ordinates also captured as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projections
- For longitude/latitude values: GCS_WGS_1984 (WKID: 4326, EPSG)
- For Eastings/Northings: OSGB1936 – British National Grid (WKID: 27700, EPSG)
- Ensure the base map/projection matches to display sites in correct locations.

## Notes
- An image (Courtesy Welsh Government) is referenced that shows the correct locations.