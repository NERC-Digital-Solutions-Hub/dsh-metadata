# Plot_locations_metadata.rtf

## Purpose and scope
- Metadata for Plot_locations.csv, which contains sampling site locations used in environmental monitoring.
- Supports consistent representation of environmental site data for assessment and policy monitoring.

## Experimental design / Sampling regime
- Three transects, each 75 m long, spaced 20 m apart, across a hillslope perpendicular to the River Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock at specified locations in Plot_locations.csv.
- Some locations have a second borehole labeled 'new'; these are equivalent to the 'old' boreholes.

## Data collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
- Also recorded as six-figure Ordnance Survey National Grid references.

## Data structure (Plot_locations.csv)
- 8 columns:
  - Name (Site identifier)
  - Latitude (decimal degrees)
  - Longitude (decimal degrees)
  - Date (measurement date)
  - Time (measurement time, GMT)
  - Easting (British National Grid)
  - Northing (British National Grid)
  - ODN (Elevation in metres above Ordnance Datum Newlyn)

## Projections / coordinate reference systems
- Ensure correct projection for proper display of sites.
- Longitude/Latitude: GCS_WGS_1984 (WKID: 4326, EPSG)
- Eastings/Northings: OSGB1936 British National Grid (WKID: 27700, EPSG)

## Notes
- An image (Courtesy Welsh Government) illustrates the correct site locations.

## Relevance for environmental analysts
- Provides standardized, QA-friendly geospatial metadata to enable accurate mapping, data integration, and transparent monitoring outputs.