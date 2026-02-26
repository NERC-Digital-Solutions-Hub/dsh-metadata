# Plot_locations_metadata.rtf

## Overview
- Metadata file for Plot_locations.csv, which contains sampling site locations.
- Describes experimental design (transects and boreholes) and methods used to collect location data.
- Includes coordinate systems, data units, and data structure details to support accurate mapping and analysis.

## Experimental design / Sampling regime
- Three transects, each 75 meters long, spaced 20 meters apart, across a hillslope perpendicular to the river Hiraethlyn.
- On each transect, four boreholes were installed down to bedrock at specified locations.
- Some locations have a second borehole labeled as 'new'; these are not functionally different from 'old' boreholes.

## Collection methods and instrumentation
- Coordinates collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude originally recorded in degrees, minutes, and seconds; converted to decimal degrees for use.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv contains the sampling site locations with 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and display notes
- Ensure the correct projection is used when displaying data:
  - Longitude/Latitude: GCS_WGS_1984 (WKID 4326; EPSG)
  - Eastings/Northings: OSGB1936 British National Grid (WKID 27700; EPSG)
- An image (courtesy Welsh Government) illustrates the correct locations; verify base map projection to display sites accurately.