# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design/sampling regime:
  - Three 75 m long transects, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
  - Boreholes labeled 'new' do not differ from those labeled 'old'.

- Collection methods and instrumentation:
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and longitude recorded as degrees, minutes, seconds and converted to decimal degrees.
  - Coordinates also recorded as six-figure Ordnance Survey National Grid references.

- Details of data structure:
  - Plot_locations.csv contains locations of sampling sites.
  - 8 columns:
    - Name (Site identifier)
    - Latitude (decimal degrees)
    - Longitude (decimal degrees)
    - Date (date of measurement)
    - Time (GMT)
    - Easting (British National Grid)
    - Northing (British National Grid)
    - ODN (Elevation in metres above Ordnance Datum Newlyn)

- Projections and base maps:
  - Longitude/latitude use GCS_WGS_1984 (WKID: 4326, EPSG).
  - Eastings/Northings use OSGB1936 British National Grid (WKID: 27700, EPSG).
  - Users should ensure correct projection for display and analysis.

- Additional notes:
  - An image courtesy of Welsh Government illustrates correct locations.