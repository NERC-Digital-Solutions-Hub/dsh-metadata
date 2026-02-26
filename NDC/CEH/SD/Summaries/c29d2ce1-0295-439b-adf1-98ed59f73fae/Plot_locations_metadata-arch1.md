# Plot_locations_metadata.rtf

- Purpose: Metadata file describing Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design: 
  - Three transects, each 75 m long and 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock at indicated locations; some locations have a second borehole labeled 'new' (these are not different from the 'old' boreholes).

- Collection methods:
  - Coordinates captured with a handheld Garmin GPS.
  - Lat/Long recorded in degrees, minutes, seconds and converted to decimal degrees.
  - Also recorded as six-figure Ordnance Survey National Grid references.

- Nature and units of recorded values:
  - Latitude and Longitude: decimal degrees (GCS_WGS_1984, WKID 4326, EPSG).
  - Easting/Northing: British National Grid (OSGB36, WKID 27700, EPSG).

- Data structure:
  - Plot_locations.csv consists of 8 columns:
    - Name: site identifier
    - Latitude: decimal degrees
    - Longitude: decimal degrees
    - Date: date of measurement
    - Time: time of measurement (Greenwich Mean Time)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: elevation in metres above Ordnance Datum Newlyn

- Projections and display notes:
  - Ensure correct projection for display and base maps to show sample sites accurately.
  - Latitude/Longitude should be shown in GCS_WGS_1984 (WKID 4326); Easting/Northing in OSGB36 / British National Grid (WKID 27700).
  - An accompanying image (Welsh Government courtesy) illustrates correct locations.

- Additional considerations:
  - The dataset supports geospatial analyses and mapping of sampling sites.
  - Time and date data enable temporal analyses alongside spatial placement.
  - The metadata emphasizes consistency in coordinate references to avoid display or interpretation errors.