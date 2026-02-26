# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design: 
  - Three transects, each 75 m long, 20 m apart, across a hillslope and perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled 'new'. 'New' boreholes do not differ from 'old'.

- Collection methods and instrumentation:
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and Longitude recorded in degrees, minutes, and seconds, converted to decimal degrees.
  - Also recorded as six-figure Ordnance Survey National Grid references.
  - Date and Time of measurement: Date and Time (Greenwich Mean Time).

- Details of data structure:
  - Plot_locations.csv contains 8 columns:
    - Name (Site identifier)
    - Latitude (decimal degrees)
    - Longitude (decimal degrees)
    - Date (date of measurement)
    - Time (time of measurement)
    - Easting (British National Grid Easting)
    - Northing (British National Grid Northing)
    - ODN (Elevation in metres above Ordnance Datum Newlyn)

- Projections / Coordinate systems:
  - Longitude and latitude use GCS_WGS_1984 (WKID: 4326, EPSG).
  - Eastings and Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).
  - Users should ensure the correct projection for display and base maps to show sample sites accurately.

- Notes on usage:
  - An image (courtesy Welsh Government) illustrates the correct locations.
  - The dataset includes elevation (ODN) and dual coordinate representations to support mapping and cross-referencing.