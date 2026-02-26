# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites.
- Plot_locations.csv provides geospatial locations for sampling transects/boreholes along a hillslope near the river Hiraethlyn.

## Experimental design and data collection
- Three transects, each 75 meters long, spaced 20 meters apart, running across the hillslope and perpendicular to the river.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled as 'new' (not different from 'old').
- Coordinates collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude recorded in decimal degrees; six-figure Ordnance Survey National Grid references also provided.

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

## Projections and display notes
- Ensure correct projection for display:
  - Longitude/Latitude values use GCS_WGS_1984 (WKID: 4326, EPSG)
  - Eastings/Northings use OSGB1936 British National Grid (WKID: 27700, EPSG)
- Base map must align with the appropriate projection to display sample sites correctly.
- An accompanying image (Welsh Government) illustrates correct locations.

## Data quality and governance notes
- The metadata clarifies data structure, coordinate systems, and measurement units to support accurate GIS usage, reproducibility, and proper data discovery.
- The file provides precise spatial context for sampling sites and boreholes, enabling consistent mapping and analysis across platforms.