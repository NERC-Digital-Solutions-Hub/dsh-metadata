# Plot_locations_metadata.rtf

## Overview
- Metadata file for Plot_locations.csv, which contains the locations of sampling sites.

## Experimental design and sampling regime
- Three transects, each 75 m long and spaced 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled 'new' (these are not different from 'old').

## Collection methods and instrumentation
- Coordinates gathered using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude originally collected in degrees, minutes, and seconds; converted to decimal degrees.
- Also recorded as six-figure Ordnance Survey (OS) National Grid references.

## Details of data structure
- Plot_locations.csv contains 8 columns:
  - Name (Site identifier)
  - Latitude (decimal degrees)
  - Longitude (decimal degrees)
  - Date (date of measurement)
  - Time (GMT)
  - Easting (British National Grid)
  - Northing (British National Grid)
  - ODN (Elevation in metres above Ordnance Datum Newlyn)

## Projection, base maps and display notes
- Correct projection is essential for accurate display:
  - Longitude/Latitude: GCS_WGS_1984 (WKID 4326, EPSG)
  - Eastings/Northings: OSGB1936 British National Grid (WKID 27700, EPSG)
- Ensure the base map uses the appropriate projection to display sample sites correctly.

## Quality, provenance and usage notes
- The dataset supports multi-coordinate representations (lat/long and OS grid) for interoperability.
- The 'new' boreholes are treated as equivalent to the 'old' boreholes in this context.
- Elevation is recorded (ODN) and coordinates include both temporal (Date, GMT Time) and spatial metadata.

## Additional notes
- An accompanying image (Courtesy Welsh Government) illustrates correct locations.