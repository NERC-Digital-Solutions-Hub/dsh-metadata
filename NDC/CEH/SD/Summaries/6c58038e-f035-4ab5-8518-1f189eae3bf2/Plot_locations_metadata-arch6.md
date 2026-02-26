# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which contains sampling site locations for a field experiment on a hillslope near the river Hiraethlyn.
- Includes borehole locations along three transects; some locations have a second borehole labeled 'new' that are equivalent to the 'old' boreholes.

## Experimental design
- Three transects, each 75 m long and 20 m apart, running perpendicular to the river.
- Along each transect, four boreholes drilled to bedrock at specified locations in Plot_locations.csv.
- Some locations include an additional borehole labeled 'new' (these are not functionally different from 'old').

## Collection methods
- Coordinates collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude captured in degrees, minutes, seconds and converted to decimal degrees.
- Also provided as six-figure Ordnance Survey National Grid references.

## Data structure (Plot_locations.csv)
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: decimal degrees
  - Longitude: decimal degrees
  - Date: date of measurement
  - Time: time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projections
- Longitude/Latitude: GCS_WGS_1984 (WKID 4326; EPSG)
- Eastings/Northings: OSGB1936 British National Grid (WKID 27700; EPSG)

## Usage notes and data quality
- Users must ensure the correct projection is selected so sample sites display in the correct locations.
- For mapping, base maps must be in the appropriate projection (WGS 84 for lat/long; OSGB for grid references).
- An image (Courtesy Welsh Government) illustrates correct locations (not included in the data file).