# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which contains the locations of sampling sites.

## Experimental design / Sampling regime
- Three 75 m long transects, 20 m apart, across a hillslope and perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at mapped locations; at some locations a second borehole was drilled.
- Boreholes labeled 'new' do not differ from those labeled 'old'.

## Collection Methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and Units of recorded values
- Latitude and longitude recorded in degrees, minutes, and seconds and converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv provides locations of sampling sites.
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and coordinate reference notes
- Longitude/Latitude values use GCS_WGS_1984 (WKID: 4326, EPSG).
- Eastings/Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).
- Correct projection must be used for display on base maps to show sample sites accurately.

## Usage notes
- An image (courtesy Welsh Government) illustrates the correct locations.

## Considerations for data governance and discoverability
- Users should verify projection consistency between data and mapping tools.
- Metadata supports locating, validating, and aligning sampling-site data within broader datasets.