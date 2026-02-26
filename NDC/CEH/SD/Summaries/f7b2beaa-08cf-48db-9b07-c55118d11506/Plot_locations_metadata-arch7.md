# Plot_locations_metadata.rtf

## Overview
- Metadata file for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design / Sampling regime
- Three transects, each 75 m long, spaced 20 m apart across a hillslope.
- Transects run perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations include a second borehole.
- Boreholes labelled 'new' do not differ from those labelled 'old'.

## Collection methods and instrumentation
- Coordinates collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
- Also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv contains locations of sampling sites and has 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and map display
- Ensure correct projection and base map to display sample sites accurately.
- Longitude/Latitude values use GCS_WGS_1984 (WKID: 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).

## Visual aid
- An accompanying image (Courtesy Welsh Government) illustrates correct locations.