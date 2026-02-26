# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design
- Three 75 m long transects, 20 m apart, across a hillslope, running perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at specified locations in Plot_locations.csv.
- At some locations a second borehole was drilled; these are labeled 'new' and do not differ from 'old'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.
- Latitude and longitude recorded in degrees, minutes, seconds, converted to decimal degrees.
- Coordinates also captured as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv provides locations of sampling sites.
- Consists of 8 columns:
  - Name (Site identifier)
  - Latitude (decimal degrees)
  - Longitude (decimal degrees)
  - Date
  - Time (GMT)
  - Easting (British National Grid)
  - Northing (British National Grid)
  - ODN (Elevation in metres above Ordnance Datum Newlyn)

## Projections and coordinate systems
- Longitude/latitude values use GCS_WGS_1984 (WKID 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID 27700, EPSG).
- Note: Users must ensure the correct projection/base map is used to display sample sites accurately.

## Display and provenance notes
- An image (Courtesy Welsh Government) illustrates the correct locations.