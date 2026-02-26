# Plot_locations_metadata.rtf

## Summary for GIS Specialists

- Purpose: Metadata for Plot_locations.csv, which stores the sampling-site locations.
- Experimental design: Three transects, each 75 m long and 20 m apart, across a hillslope and perpendicular to the river Hiraethlyn. Each transect includes four boreholes drilled to bedrock; some locations have a second borehole labeled "new" (not functionally different from "old").
- Collection methods: Coordinates captured with a handheld Garmin GPS.
- Units and coordinate formats:
  - Latitude and Longitude originally captured as degrees, minutes, seconds and converted to decimal degrees.
  - Also captured as six-figure Ordnance Survey National Grid references.
- Data structure (Plot_locations.csv): 8 columns
  - Name: Site identifier
  - Latitude: decimal degrees
  - Longitude: decimal degrees
  - Date: date of measurement
  - Time: time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn
- Projection and display notes:
  - Longitude/Latitude: GCS_WGS_1984 (WKID 4326, EPSG)
  - Easting/Northing: OSGB1936 British National Grid (WKID 27700, EPSG)
  - Users should ensure the correct projection is set on both data and base maps to display sites accurately.
- Visual aid: An image (courtesy Welsh Government) is referenced to illustrate correct locations.
- Practical implications for GIS work:
  - Data can be used to generate map-based visuals of sampling-site locations across the transects.
  - Requires transformation or consistent use of the specified projections for accurate spatial alignment.
  - Provenance and measurement times are recorded to support reproducibility and temporal analyses.