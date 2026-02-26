# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.

## Experimental design / Sampling regime
- Three 75 m long transects, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
- Boreholes labeled 'new' do not differ from those labeled 'old'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude captured in degrees, minutes, seconds and converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Details of data structure
- Plot_locations.csv comprises 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections / coordinate systems
- Longitude and latitude values use GCS_WGS_1984 (WKID 4326, EPSG).
- Eastings and Northings use OSGB1936 British National Grid (WKID 27700, EPSG).
- Correct projection must be used when displaying sample sites; base maps must be in the correct projection.
- An accompanying image (Courtesy Welsh Government) shows the correct locations.

## Data governance and provenance
- This metadata file documents Plot_locations.csv and accompanies the dataset of sampling-site locations; image reference provided for location context.

## Sharing, storage and reuse considerations
- Datasets should be uploaded to relevant portals and catalogued; maintain alignment between data and metadata.
- Ensure consistent and explicit documentation of coordinate formats and projections to support reuse.