# Plot_locations_metadata.rtf

- This file contains metadata for Plot_locations.csv, which holds the locations of sampling sites. 

## Purpose and scope
- Metadata describes the spatial locations used for sampling along transects and boreholes.

## Experimental design
- Three 75 m long transects, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
- Boreholes labeled 'new' do not differ in characteristics from those labeled 'old'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in decimal degrees (originally in degrees, minutes, seconds).
- Also recorded as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv consists of 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and display considerations
- Users must ensure correct projection for display and base maps to align sample sites.
- Longitude/Latitude use GCS_WGS_1984 (WKID 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID 27700, EPSG).

## Notable notes
- An image (Courtesy Welsh Government) illustrates the correct locations.